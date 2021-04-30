---
title: Opprette en arbeidsflyt for permisjonsforespørsel
description: Opprett en arbeidsflyt for permisjon og fravær for å behandle permisjonsforespørsler konsekvent i Dynamics 365 Human Resources.
author: andreabichsel
ms.date: 05/08/2020
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
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eb726f37d25e782a90938b7794be6dea2c30a7d5
ms.sourcegitcommit: 951393b05bf409333cb3c7ad977bcaa804aa801b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5890729"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="816dd-103">Opprette en arbeidsflyt for permisjonsforespørsel</span><span class="sxs-lookup"><span data-stu-id="816dd-103">Create a leave request workflow</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="816dd-104">Du kan opprette en arbeidsflyt i Dynamics 365 Human Resources for å behandle permisjons- og fraværsforespørsler konsekvent.</span><span class="sxs-lookup"><span data-stu-id="816dd-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="816dd-105">Med en arbeidsflyt for **permisjon og fravær** kan du:</span><span class="sxs-lookup"><span data-stu-id="816dd-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="816dd-106">Definere oppgaver</span><span class="sxs-lookup"><span data-stu-id="816dd-106">Define tasks</span></span>
- <span data-ttu-id="816dd-107">Bestemme hvem som må fullføre oppgavene</span><span class="sxs-lookup"><span data-stu-id="816dd-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="816dd-108">Angi hvem som kan godkjenne eller avvise forespørsler</span><span class="sxs-lookup"><span data-stu-id="816dd-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="816dd-109">Opprette en arbeidsflyt for permisjons- og fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="816dd-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="816dd-110">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="816dd-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="816dd-111">Under **Oppsett** velger du **Personalarbeidsflyter**.</span><span class="sxs-lookup"><span data-stu-id="816dd-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="816dd-112">Velg **Ny**, og velg deretter **Permisjons- og fraværsforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="816dd-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="816dd-113">Når meldingsboksen **Åpne denne filen?** vises, velger du **Åpne** og logger på med firmalegitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="816dd-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="816dd-114">Bruk arbeidsflytredigering til å opprette en arbeidsflyt for permisjonsforespørslene.</span><span class="sxs-lookup"><span data-stu-id="816dd-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="816dd-115">Hvis du vil ha mer informasjon om arbeidsflyter, kan du se [Oversikt over å opprette arbeidsflyter](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span><span class="sxs-lookup"><span data-stu-id="816dd-115">For more information about working with workflows, see [Create workflows overview](../fin-ops-core/fin-ops/organization-administration/create-workflow.md?toc=%2fdynamics365%2fcommerce%2ftoc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="816dd-116">Dataelementer for arbeidsflyt for permisjons- og fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="816dd-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="816dd-117">Du kan bruke følgende dataelementer til å opprette betingede eller automatiske godkjenninger i arbeidsflyter for permisjons- og fraværsforespørsler:</span><span class="sxs-lookup"><span data-stu-id="816dd-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="816dd-118">**Beløp**</span><span class="sxs-lookup"><span data-stu-id="816dd-118">**Amount**</span></span>
- <span data-ttu-id="816dd-119">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="816dd-119">**Comment**</span></span>
- <span data-ttu-id="816dd-120">**Bedrift**</span><span class="sxs-lookup"><span data-stu-id="816dd-120">**Company**</span></span>
- <span data-ttu-id="816dd-121">**Opprettet av**</span><span class="sxs-lookup"><span data-stu-id="816dd-121">**Created by**</span></span>
- <span data-ttu-id="816dd-122">**Opprettingsdato og -klokkeslett**</span><span class="sxs-lookup"><span data-stu-id="816dd-122">**Created date and time**</span></span>
- <span data-ttu-id="816dd-123">**Sluttdato**</span><span class="sxs-lookup"><span data-stu-id="816dd-123">**End date**</span></span>
- <span data-ttu-id="816dd-124">**Permisjonstype**</span><span class="sxs-lookup"><span data-stu-id="816dd-124">**Leave type**</span></span>
- <span data-ttu-id="816dd-125">**Endret av**</span><span class="sxs-lookup"><span data-stu-id="816dd-125">**Modified by**</span></span>
- <span data-ttu-id="816dd-126">**Endringsdato og -klokkeslett**</span><span class="sxs-lookup"><span data-stu-id="816dd-126">**Modified date and time**</span></span>
- <span data-ttu-id="816dd-127">**Årsakskode**</span><span class="sxs-lookup"><span data-stu-id="816dd-127">**Reason code**</span></span>
- <span data-ttu-id="816dd-128">**Forespørsels-ID**</span><span class="sxs-lookup"><span data-stu-id="816dd-128">**Request ID**</span></span>
- <span data-ttu-id="816dd-129">**Startdato**</span><span class="sxs-lookup"><span data-stu-id="816dd-129">**Start date**</span></span>
- <span data-ttu-id="816dd-130">**Status**</span><span class="sxs-lookup"><span data-stu-id="816dd-130">**Status**</span></span> 
- <span data-ttu-id="816dd-131">**Innsendingsdato**</span><span class="sxs-lookup"><span data-stu-id="816dd-131">**Submission date**</span></span>
- <span data-ttu-id="816dd-132">**Sendt av**</span><span class="sxs-lookup"><span data-stu-id="816dd-132">**Submitted by**</span></span>
- <span data-ttu-id="816dd-133">**Sendt av personalavdeling**</span><span class="sxs-lookup"><span data-stu-id="816dd-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="816dd-134">**Sendt av leder**</span><span class="sxs-lookup"><span data-stu-id="816dd-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="816dd-135">**Sendt på vegne**</span><span class="sxs-lookup"><span data-stu-id="816dd-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="816dd-136">**Worker**</span><span class="sxs-lookup"><span data-stu-id="816dd-136">**Worker**</span></span>
- <span data-ttu-id="816dd-137">**Arbeidertype**</span><span class="sxs-lookup"><span data-stu-id="816dd-137">**Worker type**</span></span>

<span data-ttu-id="816dd-138">Disse eksemplene viser hvordan du kan opprette forskjellige typer arbeidsflytbetingelser ved å bruke disse dataelementene:</span><span class="sxs-lookup"><span data-stu-id="816dd-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="816dd-139">Bruk **Årsakskode** i et betingelsesuttrykk for å rute permisjonsforespørsler for sykefravær med årsakskoden for **Operasjon** til personalavdelingen for godkjenning, mens alle andre årsakskoder rutes til prosjektlederen.</span><span class="sxs-lookup"><span data-stu-id="816dd-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="816dd-140">Hvis du vil ha mer informasjon om betingelsessetninger, se [Konfigurere betingede beslutninger i en arbeidsflyt](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="816dd-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow.md).</span></span> 

- <span data-ttu-id="816dd-141">Bruk **Sendt av personalavdeling** og **Sendt av leder** i en automatisk handling for å godkjenne permisjonsforespørsler automatisk som disse rollene sender inn på vegne av ansatte.</span><span class="sxs-lookup"><span data-stu-id="816dd-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="816dd-142">Hvis du vil ha mer informasjon om automatiske handlinger, kan du se [Konfigurere godkjenningsprosesser i en arbeidsflyt](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span><span class="sxs-lookup"><span data-stu-id="816dd-142">For more information about automatic actions, see [Configure approval processes in a workflow](../fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow.md).</span></span>

- <span data-ttu-id="816dd-143">Bruk **Permisjonstype** i en betinget setning eller automatisk handling for å kontrollere hvordan arbeidsflyten ruter forespørsler med bestemte permisjonstyper.</span><span class="sxs-lookup"><span data-stu-id="816dd-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="816dd-144">Se også</span><span class="sxs-lookup"><span data-stu-id="816dd-144">See also</span></span>

- [<span data-ttu-id="816dd-145">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="816dd-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]