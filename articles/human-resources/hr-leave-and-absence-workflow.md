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
ms.openlocfilehash: c985a0cb242fb6696b55a2514bd788ff4269f8ca
ms.sourcegitcommit: def66a9dc7feadd33411248af2545ee4a9e27c4f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/19/2020
ms.locfileid: "3385554"
---
# <a name="create-a-leave-request-workflow"></a><span data-ttu-id="dcd55-103">Opprette en arbeidsflyt for permisjonsforespørsel</span><span class="sxs-lookup"><span data-stu-id="dcd55-103">Create a leave request workflow</span></span>

<span data-ttu-id="dcd55-104">Du kan opprette en arbeidsflyt i Dynamics 365 Human Resources for å behandle permisjons- og fraværsforespørsler konsekvent.</span><span class="sxs-lookup"><span data-stu-id="dcd55-104">You can create a workflow in Dynamics 365 Human Resources to consistently manage your leave and absence requests.</span></span> <span data-ttu-id="dcd55-105">Med en arbeidsflyt for **permisjon og fravær** kan du:</span><span class="sxs-lookup"><span data-stu-id="dcd55-105">A **Leave and absence** workflow lets you:</span></span>

- <span data-ttu-id="dcd55-106">Definere oppgaver</span><span class="sxs-lookup"><span data-stu-id="dcd55-106">Define tasks</span></span>
- <span data-ttu-id="dcd55-107">Bestemme hvem som må fullføre oppgavene</span><span class="sxs-lookup"><span data-stu-id="dcd55-107">Determine who must complete the tasks</span></span>
- <span data-ttu-id="dcd55-108">Angi hvem som kan godkjenne eller avvise forespørsler</span><span class="sxs-lookup"><span data-stu-id="dcd55-108">Specify who can approve or reject requests</span></span>

## <a name="create-a-leave-and-absence-request-workflow"></a><span data-ttu-id="dcd55-109">Opprette en arbeidsflyt for permisjons- og fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="dcd55-109">Create a Leave and absence request workflow</span></span>

1. <span data-ttu-id="dcd55-110">På siden **Permisjon og fravær** velger du **Koblinger**-fanen.</span><span class="sxs-lookup"><span data-stu-id="dcd55-110">On the **Leave and absence** page, select the **Links** tab.</span></span>

2. <span data-ttu-id="dcd55-111">Under **Oppsett** velger du **Personalarbeidsflyter**.</span><span class="sxs-lookup"><span data-stu-id="dcd55-111">Under **Setup**, select **Human resource workflows**.</span></span>

3. <span data-ttu-id="dcd55-112">Velg **Ny**, og velg deretter **Permisjons- og fraværsforespørsel**.</span><span class="sxs-lookup"><span data-stu-id="dcd55-112">Select **New**, and then select **Leave and absence request**.</span></span> 

4. <span data-ttu-id="dcd55-113">Når meldingsboksen **Åpne denne filen?** vises, velger du **Åpne** og logger på med firmalegitimasjonen.</span><span class="sxs-lookup"><span data-stu-id="dcd55-113">When the **Open this file?** message box appears, select **Open** and sign in with your company credentials.</span></span>

5. <span data-ttu-id="dcd55-114">Bruk arbeidsflytredigering til å opprette en arbeidsflyt for permisjonsforespørslene.</span><span class="sxs-lookup"><span data-stu-id="dcd55-114">Use the workflow editor to create a workflow for your leave requests.</span></span> <span data-ttu-id="dcd55-115">Hvis du vil ha mer informasjon om arbeidsflyter, kan du se [Oversikt over å opprette arbeidsflyter](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span><span class="sxs-lookup"><span data-stu-id="dcd55-115">For more information about working with workflows, see [Create workflows overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/create-workflow?toc=/dynamics365/commerce/toc.json.)</span></span>

## <a name="leave-and-absence-request-workflow-data-elements"></a><span data-ttu-id="dcd55-116">Dataelementer for arbeidsflyt for permisjons- og fraværsforespørsler</span><span class="sxs-lookup"><span data-stu-id="dcd55-116">Leave and absence request workflow data elements</span></span>

<span data-ttu-id="dcd55-117">Du kan bruke følgende dataelementer til å opprette betingede eller automatiske godkjenninger i arbeidsflyter for permisjons- og fraværsforespørsler:</span><span class="sxs-lookup"><span data-stu-id="dcd55-117">You can use the following data elements to create conditional or automatic approvals in workflows for leave and absence requests:</span></span>

- <span data-ttu-id="dcd55-118">**Beløp**</span><span class="sxs-lookup"><span data-stu-id="dcd55-118">**Amount**</span></span>
- <span data-ttu-id="dcd55-119">**Kommentar**</span><span class="sxs-lookup"><span data-stu-id="dcd55-119">**Comment**</span></span>
- <span data-ttu-id="dcd55-120">**Bedrift**</span><span class="sxs-lookup"><span data-stu-id="dcd55-120">**Company**</span></span>
- <span data-ttu-id="dcd55-121">**Opprettet av**</span><span class="sxs-lookup"><span data-stu-id="dcd55-121">**Created by**</span></span>
- <span data-ttu-id="dcd55-122">**Opprettingsdato og -klokkeslett**</span><span class="sxs-lookup"><span data-stu-id="dcd55-122">**Created date and time**</span></span>
- <span data-ttu-id="dcd55-123">**Sluttdato**</span><span class="sxs-lookup"><span data-stu-id="dcd55-123">**End date**</span></span>
- <span data-ttu-id="dcd55-124">**Permisjonstype**</span><span class="sxs-lookup"><span data-stu-id="dcd55-124">**Leave type**</span></span>
- <span data-ttu-id="dcd55-125">**Endret av**</span><span class="sxs-lookup"><span data-stu-id="dcd55-125">**Modified by**</span></span>
- <span data-ttu-id="dcd55-126">**Endringsdato og -klokkeslett**</span><span class="sxs-lookup"><span data-stu-id="dcd55-126">**Modified date and time**</span></span>
- <span data-ttu-id="dcd55-127">**Årsakskode**</span><span class="sxs-lookup"><span data-stu-id="dcd55-127">**Reason code**</span></span>
- <span data-ttu-id="dcd55-128">**Forespørsels-ID**</span><span class="sxs-lookup"><span data-stu-id="dcd55-128">**Request ID**</span></span>
- <span data-ttu-id="dcd55-129">**Startdato**</span><span class="sxs-lookup"><span data-stu-id="dcd55-129">**Start date**</span></span>
- <span data-ttu-id="dcd55-130">**Status**</span><span class="sxs-lookup"><span data-stu-id="dcd55-130">**Status**</span></span> 
- <span data-ttu-id="dcd55-131">**Innsendingsdato**</span><span class="sxs-lookup"><span data-stu-id="dcd55-131">**Submission date**</span></span>
- <span data-ttu-id="dcd55-132">**Sendt av**</span><span class="sxs-lookup"><span data-stu-id="dcd55-132">**Submitted by**</span></span>
- <span data-ttu-id="dcd55-133">**Sendt av personalavdeling**</span><span class="sxs-lookup"><span data-stu-id="dcd55-133">**Submitted by Human resources**</span></span>
- <span data-ttu-id="dcd55-134">**Sendt av leder**</span><span class="sxs-lookup"><span data-stu-id="dcd55-134">**Submitted by Manager**</span></span>
- <span data-ttu-id="dcd55-135">**Sendt på vegne**</span><span class="sxs-lookup"><span data-stu-id="dcd55-135">**Submitted on behalf**</span></span>
- <span data-ttu-id="dcd55-136">**Worker**</span><span class="sxs-lookup"><span data-stu-id="dcd55-136">**Worker**</span></span>
- <span data-ttu-id="dcd55-137">**Arbeidertype**</span><span class="sxs-lookup"><span data-stu-id="dcd55-137">**Worker type**</span></span>

<span data-ttu-id="dcd55-138">Disse eksemplene viser hvordan du kan opprette forskjellige typer arbeidsflytbetingelser ved å bruke disse dataelementene:</span><span class="sxs-lookup"><span data-stu-id="dcd55-138">These examples show how you can create different types of workflow conditions by using these data elements:</span></span>

- <span data-ttu-id="dcd55-139">Bruk **Årsakskode** i et betingelsesuttrykk for å rute permisjonsforespørsler for sykefravær med årsakskoden for **Operasjon** til personalavdelingen for godkjenning, mens alle andre årsakskoder rutes til prosjektlederen.</span><span class="sxs-lookup"><span data-stu-id="dcd55-139">Use **Reason code** in a conditional statement to route sick leave requests with the reason code **Surgery** to HR for approval, while routing all other reason codes to the manager.</span></span> <span data-ttu-id="dcd55-140">Hvis du vil ha mer informasjon om betingelsessetninger, se [Konfigurere betingede beslutninger i en arbeidsflyt](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span><span class="sxs-lookup"><span data-stu-id="dcd55-140">For more information about conditional statements, see [Configure conditional decisions in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-conditional-decision-workflow).</span></span> 

- <span data-ttu-id="dcd55-141">Bruk **Sendt av personalavdeling** og **Sendt av leder** i en automatisk handling for å godkjenne permisjonsforespørsler automatisk som disse rollene sender inn på vegne av ansatte.</span><span class="sxs-lookup"><span data-stu-id="dcd55-141">Use **Submitted by Human resources** and **Submitted by manager** in an automatic action to automatically approve leave requests that these roles submit on behalf of employees.</span></span> <span data-ttu-id="dcd55-142">Hvis du vil ha mer informasjon om automatiske handlinger, kan du se [Konfigurere godkjenningsprosesser i en arbeidsflyt](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span><span class="sxs-lookup"><span data-stu-id="dcd55-142">For more information about automatic actions, see [Configure approval processes in a workflow](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/organization-administration/configure-approval-process-workflow).</span></span>

- <span data-ttu-id="dcd55-143">Bruk **Permisjonstype** i en betinget setning eller automatisk handling for å kontrollere hvordan arbeidsflyten ruter forespørsler med bestemte permisjonstyper.</span><span class="sxs-lookup"><span data-stu-id="dcd55-143">Use **Leave type** in a conditional statement or automatic action to control how the workflow routes requests with certain leave types.</span></span>

## <a name="see-also"></a><span data-ttu-id="dcd55-144">Se også</span><span class="sxs-lookup"><span data-stu-id="dcd55-144">See also</span></span>

- [<span data-ttu-id="dcd55-145">Oversikt over permisjon og fravær</span><span class="sxs-lookup"><span data-stu-id="dcd55-145">Leave and absence overview</span></span>](hr-leave-and-absence-overview.md)
