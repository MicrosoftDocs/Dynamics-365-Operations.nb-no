---
title: Opprette en arbeidsflyt for forespørsel om kjøp og salg av permisjon
description: Opprett en arbeidsflyt for forespørsel om kjøp og salg av permisjon for å kjøpe og selge permisjonsforespørsler konsekvent i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 08/20/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: LeavePlanFormPart, LeaveAbsenceWorkspace
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-08-20
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 15cedc16fbdbb5d25daa262f094a56bb8fe2f5cc
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5892711"
---
# <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="23a44-103">Opprette en arbeidsflyt for forespørsel om kjøp og salg av permisjon</span><span class="sxs-lookup"><span data-stu-id="23a44-103">Create a buy and sell leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="23a44-104">Du kan opprette en arbeidsflyt i Dynamics 365 Human Resources for å behandle kjøps- og salgsforespørsler konsekvent.</span><span class="sxs-lookup"><span data-stu-id="23a44-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your buy and sell leave requests.</span></span> <span data-ttu-id="23a44-105">Med en arbeidsflyt for **Kjøp og selg permisjon** kan du:</span><span class="sxs-lookup"><span data-stu-id="23a44-105">A **Buy and sell leave** workflow lets you:</span></span>

- <span data-ttu-id="23a44-106">Definere oppgaver</span><span class="sxs-lookup"><span data-stu-id="23a44-106">Define tasks</span></span>
- <span data-ttu-id="23a44-107">Bestemme hvem som må fullføre oppgavene</span><span class="sxs-lookup"><span data-stu-id="23a44-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="23a44-108">Angi hvem som kan godkjenne eller avvise forespørsler</span><span class="sxs-lookup"><span data-stu-id="23a44-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-buy-and-sell-leave-request-workflow"></a><span data-ttu-id="23a44-109">Opprette en arbeidsflyt for forespørsel om kjøp og salg av permisjon</span><span class="sxs-lookup"><span data-stu-id="23a44-109">Create a buy and sell leave request workflow</span></span>

1. <span data-ttu-id="23a44-110">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="23a44-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="23a44-111">Under **Oppsett** velger du **Personalarbeidsflyter**.</span><span class="sxs-lookup"><span data-stu-id="23a44-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="23a44-112">Velg **Ny**, og velg deretter **Forespørsel om kjøp og salg av permisjon**.</span><span class="sxs-lookup"><span data-stu-id="23a44-112">Select **New**, and then select **Buy and sell leave request**.</span></span> 

4. <span data-ttu-id="23a44-113">Når meldingsboksen **Åpne denne filen?** vises, velger du **Åpne** og logger på med firmalegitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="23a44-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="23a44-114">Bruk arbeidsflytredigering til å opprette en arbeidsflyt for permisjonsforespørslene.</span><span class="sxs-lookup"><span data-stu-id="23a44-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="23a44-115">Hvis du vil ha mer informasjon om arbeidsflyter, kan du se [Oversikt over å opprette arbeidsflyter](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span><span class="sxs-lookup"><span data-stu-id="23a44-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="23a44-116">Dataelementer for arbeidsflyt for permisjons- og fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="23a44-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="23a44-117">Du kan bruke følgende dataelementer til å opprette betingede eller automatiske godkjenninger i arbeidsflyter for forespørsler om kjøp og salg av permisjon:</span><span class="sxs-lookup"><span data-stu-id="23a44-117">You can use the following data elements to create conditional or automatic approvals in workflows for buy and sell leave requests:</span></span>

- <span data-ttu-id="23a44-118">**Beløp**</span><span class="sxs-lookup"><span data-stu-id="23a44-118">**Amount**</span></span>
- <span data-ttu-id="23a44-119">**Kjøps- og salgspolicy for permisjon**</span><span class="sxs-lookup"><span data-stu-id="23a44-119">**Buy and sell leave policy**</span></span>
- <span data-ttu-id="23a44-120">**Bedrift**</span><span class="sxs-lookup"><span data-stu-id="23a44-120">**Company**</span></span>
- <span data-ttu-id="23a44-121">**Opprettet av**</span><span class="sxs-lookup"><span data-stu-id="23a44-121">**Created by**</span></span>
- <span data-ttu-id="23a44-122">**Opprettingsdato og -klokkeslett**</span><span class="sxs-lookup"><span data-stu-id="23a44-122">**Created date and time**</span></span>
- <span data-ttu-id="23a44-123">**Sluttdato**</span><span class="sxs-lookup"><span data-stu-id="23a44-123">**End date**</span></span>
- <span data-ttu-id="23a44-124">**Permisjonstype**</span><span class="sxs-lookup"><span data-stu-id="23a44-124">**Leave type**</span></span>
- <span data-ttu-id="23a44-125">**Endret av**</span><span class="sxs-lookup"><span data-stu-id="23a44-125">**Modified by**</span></span>
- <span data-ttu-id="23a44-126">**Endringsdato og -klokkeslett**</span><span class="sxs-lookup"><span data-stu-id="23a44-126">**Modified date and time**</span></span>
- <span data-ttu-id="23a44-127">**Forespørsels-ID**</span><span class="sxs-lookup"><span data-stu-id="23a44-127">**Request ID**</span></span>
- <span data-ttu-id="23a44-128">**Startdato**</span><span class="sxs-lookup"><span data-stu-id="23a44-128">**Start date**</span></span>
- <span data-ttu-id="23a44-129">**Status**</span><span class="sxs-lookup"><span data-stu-id="23a44-129">**Status**</span></span> 
- <span data-ttu-id="23a44-130">**Innsendingsdato**</span><span class="sxs-lookup"><span data-stu-id="23a44-130">**Submission date**</span></span>
- <span data-ttu-id="23a44-131">**Sendt av**</span><span class="sxs-lookup"><span data-stu-id="23a44-131">**Submitted by**</span></span>
- <span data-ttu-id="23a44-132">**Sendt av personalavdeling**</span><span class="sxs-lookup"><span data-stu-id="23a44-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="23a44-133">**Sendt av leder**</span><span class="sxs-lookup"><span data-stu-id="23a44-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="23a44-134">**Sendt på vegne**</span><span class="sxs-lookup"><span data-stu-id="23a44-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="23a44-135">**Worker**</span><span class="sxs-lookup"><span data-stu-id="23a44-135">**Worker**</span></span>

## <a name="workflow-examples"></a><span data-ttu-id="23a44-136">Arbeidsflyteksempler</span><span class="sxs-lookup"><span data-stu-id="23a44-136">Workflow examples</span></span>

<span data-ttu-id="23a44-137">Disse eksemplene viser hvordan du kan opprette forskjellige typer arbeidsflytbetingelser ved å bruke disse dataelementene:</span><span class="sxs-lookup"><span data-stu-id="23a44-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="23a44-138">Bruk **Sendt av personalavdeling** og **Sendt av leder** i en automatisk handling for å godkjenne permisjonsforespørsler for kjøp og salg automatisk som disse rollene sender inn på vegne av ansatte.</span><span class="sxs-lookup"><span data-stu-id="23a44-138">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve buy and sell leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="23a44-139">Hvis du vil ha mer informasjon om automatiske handlinger, kan du se [Konfigurere godkjenningsprosesser i en arbeidsflyt](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="23a44-139">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="23a44-140">Bruk **Permisjonstype** i en betinget setning eller automatisk handling for å kontrollere hvordan arbeidsflyten ruter forespørsler med bestemte permisjonstyper.</span><span class="sxs-lookup"><span data-stu-id="23a44-140">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="23a44-141">Se også</span><span class="sxs-lookup"><span data-stu-id="23a44-141">See also</span></span>

[<span data-ttu-id="23a44-142">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="23a44-142">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)<br>
[<span data-ttu-id="23a44-143">Administrere policyer for kjøp og salg av permisjon</span><span class="sxs-lookup"><span data-stu-id="23a44-143">Manage buy and sell leave policies</span></span>](hr-leave-and-absence-manage-buy-and-sell-leave-policies.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]