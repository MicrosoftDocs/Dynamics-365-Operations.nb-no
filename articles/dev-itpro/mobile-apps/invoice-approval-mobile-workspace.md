---
title: "Mobilt arbeidsområde for fakturagodkjenning"
description: "Dette emnet gir informasjon om det mobile arbeidsområdet for fakturagodkjenning. Dette arbeidsområdet gir en liste over fakturaer som er tilordnet til deg gjennom arbeidsflytprosessen leverandørfakturahode."
author: abruer
manager: AnnBe
ms.date: 06/16/2017
ms.topic: article
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: sericks
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: abruer
ms.search.validFrom: 2017-06-30
ms.dyn365.ops.version: July 2017 update
ms.translationtype: HT
ms.sourcegitcommit: 2771a31b5a4d418a27de0ebe1945d1fed2d8d6d6
ms.openlocfilehash: af673f076f684500b6ca84d04c01f7f773d65cd6
ms.contentlocale: nb-no
ms.lasthandoff: 11/03/2017

---

# <a name="invoice-approvals-mobile-workspace"></a><span data-ttu-id="2e920-104">Mobilt arbeidsområde for fakturagodkjenning</span><span class="sxs-lookup"><span data-stu-id="2e920-104">Invoice approvals mobile workspace</span></span>

[!include[banner](../includes/banner.md)]

<span data-ttu-id="2e920-105">Dette emnet gir informasjon om det mobile arbeidsområdet **Fakturagodkjenning**.</span><span class="sxs-lookup"><span data-stu-id="2e920-105">This topic provides information about the **Invoice approvals** mobile workspace.</span></span> <span data-ttu-id="2e920-106">Dette arbeidsområdet gir en liste over fakturaer som er tilordnet til deg gjennom arbeidsflytprosessen leverandørfakturahode.</span><span class="sxs-lookup"><span data-stu-id="2e920-106">This workspace provides a list of invoices that have been assigned to you through the vendor invoice header workflow process.</span></span> 

<span data-ttu-id="2e920-107">Dette mobile arbeidsområdet er ment å brukes med mobilappen Microsoft Dynamics 365 for Unified Operations.</span><span class="sxs-lookup"><span data-stu-id="2e920-107">This mobile workspace is intended to be used with the Microsoft Dynamics 365 for Unified Operations mobile app.</span></span>

## <a name="overview"></a><span data-ttu-id="2e920-108">Oversikt</span><span class="sxs-lookup"><span data-stu-id="2e920-108">Overview</span></span>

<span data-ttu-id="2e920-109">Med det mobilie arbeidsområdet **Fakturagodkjenninger**  kan regnskapsassistenter og -sjefer vise fakturaene som er tilordnet til dem, som en del av arbeidsflytprosessen leverandørfakturahode.</span><span class="sxs-lookup"><span data-stu-id="2e920-109">The **Invoice approvals** mobile workspace lets Accounts payable clerks and managers view invoices that have been assigned to them as part of the vendor invoice header workflow process.</span></span> <span data-ttu-id="2e920-110">Du kan vise fakturainformasjon, og til og med linje- og distribusjonsdetaljer, som hjelper deg å ta informerte beslutninger om godkjenning.</span><span class="sxs-lookup"><span data-stu-id="2e920-110">You can view the invoice information, and even the line and distribution details, to help you make informed approval decisions.</span></span> <span data-ttu-id="2e920-111">Fra arbeidsområdet kan du utføre handlinger for å flytte fakturaen gjennom arbeidsflytprosessen.</span><span class="sxs-lookup"><span data-stu-id="2e920-111">From the workspace, you can take action to move the invoice through the workflow process.</span></span> 

## <a name="prerequisites"></a><span data-ttu-id="2e920-112">Forutsetninger</span><span class="sxs-lookup"><span data-stu-id="2e920-112">Prerequisites</span></span>

<span data-ttu-id="2e920-113">Før du kan bruke dette mobile arbeidsområdet, må du oppfylle følgende forutsetninger.</span><span class="sxs-lookup"><span data-stu-id="2e920-113">Before you can use this mobile workspace, the following prerequisites must be met.</span></span>

<table>
<thead>
<tr class="header">
<th><span data-ttu-id="2e920-114">Forutsetning</span><span class="sxs-lookup"><span data-stu-id="2e920-114">Prerequisite</span></span></th>
<th><span data-ttu-id="2e920-115">Rolle</span><span class="sxs-lookup"><span data-stu-id="2e920-115">Role</span></span></th>
<th><span data-ttu-id="2e920-116">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="2e920-116">Description</span></span></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><span data-ttu-id="2e920-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise Edition (juli 2017) må være distribuert i organisasjonen din.</span><span class="sxs-lookup"><span data-stu-id="2e920-117">Microsoft Dynamics 365 for Finance and Operations, Enterprise edition (July 2017) must be deployed in your organization.</span></span></td>
<td><span data-ttu-id="2e920-118">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="2e920-118">System administrator</span></span></td>
<td><span data-ttu-id="2e920-119">Se <a href="../deployment/deploy-demo-environment.md">Distribuere et demomiljø</a>.</span><span class="sxs-lookup"><span data-stu-id="2e920-119">See <a href="../deployment/deploy-demo-environment.md">Deploy a demo environment</a>.</span></span>
</td>
</tr>
<tr class="even">
<td><span data-ttu-id="2e920-120">Det mobile arbeidsområdet <strong>Fakturagodkjenning</strong> må publiseres.</span><span class="sxs-lookup"><span data-stu-id="2e920-120">The <strong>Invoice approvals</strong> mobile workspace must be published.</span></span></td>
<td><span data-ttu-id="2e920-121">Systemansvarlig</span><span class="sxs-lookup"><span data-stu-id="2e920-121">System administrator</span></span></td>
<td><span data-ttu-id="2e920-122">Se <a href="publish-mobile-workspace.md">Publisere et mobilt arbeidsområde</a>.</span><span class="sxs-lookup"><span data-stu-id="2e920-122">See <a href="publish-mobile-workspace.md">Publish a mobile workspace</a>.</span></span></td>
</tr>
</tbody>
</table>

## <a name="download-and-install-the-mobile-app"></a><span data-ttu-id="2e920-123">Laste ned og installere mobilappen</span><span class="sxs-lookup"><span data-stu-id="2e920-123">Download and install the mobile app</span></span>

<span data-ttu-id="2e920-124">Last ned og installer mobilappen Dynamics 365 for Unified Operations:</span><span class="sxs-lookup"><span data-stu-id="2e920-124">Download and install the Dynamics 365 for Unified Operations mobile app:</span></span>

-   [<span data-ttu-id="2e920-125">For Android-telefoner</span><span class="sxs-lookup"><span data-stu-id="2e920-125">For Android phones</span></span>](https://go.microsoft.com/fwlink/?linkid=850662)
-   [<span data-ttu-id="2e920-126">For iPhone</span><span class="sxs-lookup"><span data-stu-id="2e920-126">For iPhones</span></span>](https://go.microsoft.com/fwlink/?linkid=850663)

## <a name="sign-in-to-the-mobile-app"></a><span data-ttu-id="2e920-127">Logge på mobilappen</span><span class="sxs-lookup"><span data-stu-id="2e920-127">Sign in to the mobile app</span></span>

1.  <span data-ttu-id="2e920-128">Start appen på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="2e920-128">Start the app on your mobile device.</span></span>
2.  <span data-ttu-id="2e920-129">Skriv inn URL-adressen til Microsoft Dynamics 365.</span><span class="sxs-lookup"><span data-stu-id="2e920-129">Enter your Microsoft Dynamics 365 URL.</span></span>
3.  <span data-ttu-id="2e920-130">Første gang du logger deg på, blir du bedt om brukernavn og passord.</span><span class="sxs-lookup"><span data-stu-id="2e920-130">The first time that you sign in, you're prompted for your user name and password.</span></span> <span data-ttu-id="2e920-131">Angi legitimasjon.</span><span class="sxs-lookup"><span data-stu-id="2e920-131">Enter your credentials.</span></span>
4.  <span data-ttu-id="2e920-132">Når du har logget deg på, vises tilgjengelige arbeidsområder for firmaet.</span><span class="sxs-lookup"><span data-stu-id="2e920-132">After you sign in, the available workspaces for your company are shown.</span></span> <span data-ttu-id="2e920-133">Legg merke til at hvis systemansvarlig senere publiserer et nytt arbeidsområde, må du oppdatere listen over mobile arbeidsområder.</span><span class="sxs-lookup"><span data-stu-id="2e920-133">Note that if your system administrator publishes a new workspace later, you will have to refresh the list of mobile workspaces.</span></span>

    <span data-ttu-id="2e920-134">[![Hent for å oppdatere](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span><span class="sxs-lookup"><span data-stu-id="2e920-134">[![Pull to refresh](./media/pull-to-refresh-list-of-workspaces-183x300.png)](./media/pull-to-refresh-list-of-workspaces.png)</span></span>

## <a name="approve-invoices-by-using-the-invoice-approvals-mobile-workspace"></a><span data-ttu-id="2e920-135">Godkjenne fakturaer ved hjelp av det mobile arbeidsrområdet Fakturagodkjenning</span><span class="sxs-lookup"><span data-stu-id="2e920-135">Approve invoices by using the Invoice approvals mobile workspace</span></span>
1.  <span data-ttu-id="2e920-136">Velg **Fakturagodkjenning**-arbeidsområdet på mobilenheten.</span><span class="sxs-lookup"><span data-stu-id="2e920-136">On your mobile device, select the **Invoice approvals** workspace.</span></span>
2.  <span data-ttu-id="2e920-137">Velg fakturaen som er tilordnet til deg av arbeidsflytprosessen leverandørfakturahode.</span><span class="sxs-lookup"><span data-stu-id="2e920-137">Select the invoice that has been assigned to you by the vendor invoice header workflow process.</span></span>
3.  <span data-ttu-id="2e920-138">På siden **Fakturaopplysninger** kan du se gjennom fakturahodeinformasjonen, for eksempel leverandør- og datoinformasjon.</span><span class="sxs-lookup"><span data-stu-id="2e920-138">On the **Invoice details** page, review the invoice header information, such as the vendor and date information.</span></span>
4.  <span data-ttu-id="2e920-139">Velg en linje på fakturaen for å vise mer detaljert informasjon om den i  **fakturalinjedetaljer**-visningen.</span><span class="sxs-lookup"><span data-stu-id="2e920-139">Select a line on the invoice to view more detailed information about it in the **Invoice line details** view.</span></span>
5.  <span data-ttu-id="2e920-140">I visningen **Fakturalinjedetaljer** velger du **Distribusjoner** for å vise linjedistribusjonene.</span><span class="sxs-lookup"><span data-stu-id="2e920-140">In the **Invoice line details** view, select **Distributions** to show the line distributions.</span></span> <span data-ttu-id="2e920-141">Her kan du vise regnskapet for fakturalinjen.</span><span class="sxs-lookup"><span data-stu-id="2e920-141">Here, you can view the accounting for the invoice line.</span></span> <span data-ttu-id="2e920-142">Informasjonen som vises, inkluderer finansdimensjonene og hovedkontoen.</span><span class="sxs-lookup"><span data-stu-id="2e920-142">The information that is shown includes the financial dimensions and the main account.</span></span>
6.  <span data-ttu-id="2e920-143">På siden **Fakturadetaljer** velger du **Distribusjoner** for å vise alle distribusjonene.</span><span class="sxs-lookup"><span data-stu-id="2e920-143">On the **Invoice details** page, select **Distributions** to show all distributions.</span></span> <span data-ttu-id="2e920-144">Her kan du vise regnskapet for hele fakturaen.</span><span class="sxs-lookup"><span data-stu-id="2e920-144">Here, you can view the accounting for the whole invoice.</span></span> <span data-ttu-id="2e920-145">Informasjonen som vises, inkluderer finansdimensjonene og hovedkontoene.</span><span class="sxs-lookup"><span data-stu-id="2e920-145">The information that is shown includes the financial dimensions and the main accounts.</span></span> 
7.  <span data-ttu-id="2e920-146">Velg **Vedlegg** for å vise notater eller filer som er knyttet til fakturaen.</span><span class="sxs-lookup"><span data-stu-id="2e920-146">Select **Attachments** to view any notes or files that are attached to the invoice.</span></span>
8.  <span data-ttu-id="2e920-147">På siden **Fakturadetaljer** velger du riktig handling i arbeidsflyten forl å fullføre gjennomgangen.</span><span class="sxs-lookup"><span data-stu-id="2e920-147">On the **Invoice details** page, select the appropriate workflow action to complete your review process.</span></span>
9.  <span data-ttu-id="2e920-148">Velg **Ferdig**.</span><span class="sxs-lookup"><span data-stu-id="2e920-148">Select **Done**.</span></span>

