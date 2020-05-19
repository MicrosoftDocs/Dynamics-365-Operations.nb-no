---
title: Opprette en arbeidsflyt for permisjonsforespørsel
description: Opprett en arbeidsflyt for permisjon og fravær for å behandle permisjonsforespørsler konsekvent i Dynamics 365 Human Resources.
author: andreabichsel
manager: AnnBe
ms.date: 05/08/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2e994d11bbd45907a48c1f3955fa751a676a327
ms.sourcegitcommit: e69cfc74e9dbce64ae0e1ab7cd441e5ae6efd4c9
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/08/2020
ms.locfileid: "3353694"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="52493-103">Opprette en arbeidsflyt for permisjonsforespørsel</span><span class="sxs-lookup"><span data-stu-id="52493-103">Create a leave request workflow</span></span>

<span data-ttu-id="52493-104">Du kan opprette en arbeidsflyt i Dynamics 365 Human Resources for å behandle permisjons- og fraværsforespørsler konsekvent.</span><span class="sxs-lookup"><span data-stu-id="52493-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="52493-105">Med en arbeidsflyt for **permisjon og fravær** kan du:</span><span class="sxs-lookup"><span data-stu-id="52493-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="52493-106">Definere oppgaver</span><span class="sxs-lookup"><span data-stu-id="52493-106">Define tasks</span></span>
- <span data-ttu-id="52493-107">Bestemme hvem som må fullføre oppgavene</span><span class="sxs-lookup"><span data-stu-id="52493-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="52493-108">Angi hvem som kan godkjenne eller avvise forespørsler</span><span class="sxs-lookup"><span data-stu-id="52493-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="52493-109">Opprette en arbeidsflyt for permisjons- og fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="52493-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="52493-110">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="52493-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="52493-111">Under **Oppsett** velger du **Personalarbeidsflyter**.</span><span class="sxs-lookup"><span data-stu-id="52493-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="52493-112">Velg **Ny**, og velg deretter **Permisjons- og fraværsforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="52493-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="52493-113">Når meldingsboksen **Åpne denne filen?** vises, velger du **Åpne** og logger på med firmalegitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="52493-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="52493-114">Bruk arbeidsflytredigering til å opprette en arbeidsflyt for permisjonsforespørslene.</span><span class="sxs-lookup"><span data-stu-id="52493-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="52493-115">Hvis du vil ha mer informasjon om arbeidsflyter, kan du se [Oversikt over å opprette arbeidsflyter](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="52493-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="52493-116">Dataelementer for arbeidsflyt for permisjons- og fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="52493-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="52493-117">Du kan bruke følgende dataelementer til å opprette betingede eller automatiske godkjenninger i arbeidsflyter for permisjons- og fraværsforespørsler:</span><span class="sxs-lookup"><span data-stu-id="52493-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="52493-118">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="52493-118">**Comment**</span></span>
- <span data-ttu-id="52493-119">**Bedrift**</span><span class="sxs-lookup"><span data-stu-id="52493-119">**Company**</span></span>
- <span data-ttu-id="52493-120">**Opprettet av**</span><span class="sxs-lookup"><span data-stu-id="52493-120">**Created by**</span></span>
- <span data-ttu-id="52493-121">**Opprettingsdato og -klokkeslett**</span><span class="sxs-lookup"><span data-stu-id="52493-121">**Created date and time**</span></span>
- <span data-ttu-id="52493-122">**Sluttdato**</span><span class="sxs-lookup"><span data-stu-id="52493-122">**End date**</span></span>
- <span data-ttu-id="52493-123">**Permisjonstype**</span><span class="sxs-lookup"><span data-stu-id="52493-123">**Leave type**</span></span>
- <span data-ttu-id="52493-124">**Endret av**</span><span class="sxs-lookup"><span data-stu-id="52493-124">**Modified by**</span></span>
- <span data-ttu-id="52493-125">**Endringsdato og -klokkeslett**</span><span class="sxs-lookup"><span data-stu-id="52493-125">**Modified date and time**</span></span>
- <span data-ttu-id="52493-126">**Årsakskode**</span><span class="sxs-lookup"><span data-stu-id="52493-126">**Reason code**</span></span>
- <span data-ttu-id="52493-127">**Forespørsels-ID**</span><span class="sxs-lookup"><span data-stu-id="52493-127">**Request ID**</span></span>
- <span data-ttu-id="52493-128">**Startdato**</span><span class="sxs-lookup"><span data-stu-id="52493-128">**Start date**</span></span>
- <span data-ttu-id="52493-129">**Status**</span><span class="sxs-lookup"><span data-stu-id="52493-129">**Status**</span></span> 
- <span data-ttu-id="52493-130">**Innsendingsdato**</span><span class="sxs-lookup"><span data-stu-id="52493-130">**Submission date**</span></span>
- <span data-ttu-id="52493-131">**Sendt av**</span><span class="sxs-lookup"><span data-stu-id="52493-131">**Submitted by**</span></span>
- <span data-ttu-id="52493-132">**Sendt av personalavdeling**</span><span class="sxs-lookup"><span data-stu-id="52493-132">**Submitted by Human resources**</span></span>
- <span data-ttu-id="52493-133">**Sendt av leder**</span><span class="sxs-lookup"><span data-stu-id="52493-133">**Submitted by Manager**</span></span>
- <span data-ttu-id="52493-134">**Sendt på vegne**</span><span class="sxs-lookup"><span data-stu-id="52493-134">**Submitted on behalf**</span></span>
- <span data-ttu-id="52493-135">**Worker**</span><span class="sxs-lookup"><span data-stu-id="52493-135">**Worker**</span></span>
- <span data-ttu-id="52493-136">**Arbeidertype**</span><span class="sxs-lookup"><span data-stu-id="52493-136">**Worker type**</span></span>

<span data-ttu-id="52493-137">Disse eksemplene viser hvordan du kan opprette forskjellige typer arbeidsflytbetingelser ved å bruke disse dataelementene:</span><span class="sxs-lookup"><span data-stu-id="52493-137">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="52493-138">Bruk **Årsakskode** i et betingelsesuttrykk for å rute permisjonsforespørsler for sykefravær med årsakskoden for **Operasjon** til personalavdelingen for godkjenning, mens alle andre årsakskoder rutes til prosjektlederen.</span><span class="sxs-lookup"><span data-stu-id="52493-138">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="52493-139">Hvis du vil ha mer informasjon om betingelsessetninger, se [Konfigurere betingede beslutninger i en arbeidsflyt](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="52493-139">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="52493-140">Bruk **Sendt av personalavdeling** og **Sendt av leder** i en automatisk handling for å godkjenne permisjonsforespørsler automatisk som disse rollene sender inn på vegne av ansatte.</span><span class="sxs-lookup"><span data-stu-id="52493-140">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="52493-141">Hvis du vil ha mer informasjon om automatiske handlinger, kan du se [Konfigurere godkjenningsprosesser i en arbeidsflyt](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="52493-141">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="52493-142">Bruk **Permisjonstype** i en betinget setning eller automatisk handling for å kontrollere hvordan arbeidsflyten ruter forespørsler med bestemte permisjonstyper.</span><span class="sxs-lookup"><span data-stu-id="52493-142">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="52493-143">Se også</span><span class="sxs-lookup"><span data-stu-id="52493-143">See also</span></span>

- [<span data-ttu-id="52493-144">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="52493-144">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
