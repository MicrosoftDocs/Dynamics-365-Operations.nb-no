---
title: Hva er nytt eller endret i Dynamics 365 Talent (5. november 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 11/05/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-talent
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Talent
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: dkrame
ms.search.validFrom: 2019-11-05
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 48de07178acfaccf11e0a02b2848bf24e6ccc117
ms.sourcegitcommit: 871707a3fd236da693a3d51f401eb0cb9d4bae39
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 12/06/2019
ms.locfileid: "2896779"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-november-5-2019"></a><span data-ttu-id="9eeb5-103">Hva er nytt eller endret i Dynamics 365 Talent (5. november 2019)</span><span class="sxs-lookup"><span data-stu-id="9eeb5-103">What's new or changed in Dynamics 365 Talent (November 5, 2019)</span></span>

<span data-ttu-id="9eeb5-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="9eeb5-105">Endringer i Attract</span><span class="sxs-lookup"><span data-stu-id="9eeb5-105">Changes in Attract</span></span>

<span data-ttu-id="9eeb5-106">Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="9eeb5-107">Endringer i Onboard</span><span class="sxs-lookup"><span data-stu-id="9eeb5-107">Changes in Onboard</span></span>

<span data-ttu-id="9eeb5-108">Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="9eeb5-109">Endringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="9eeb5-109">Changes in Core HR</span></span>

<span data-ttu-id="9eeb5-110">Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2598.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-110">Changes described in this section apply to build number 8.1.2598.</span></span> <span data-ttu-id="9eeb5-111">Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="9eeb5-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="copy-a-core-hr-instance"></a><span data-ttu-id="9eeb5-112">Kopiere en Core HR-forekomst</span><span class="sxs-lookup"><span data-stu-id="9eeb5-112">Copy a Core HR instance</span></span>

<span data-ttu-id="9eeb5-113">I denne ukes versjonen kan du bruke Microsoft Dynamics Lifecycle Services (LCS) til å kopiere en Microsoft Dynamics 365 Talent: Core HR-database til et sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-113">In this week's release, you can use Microsoft Dynamics Lifecycle Services (LCS) to copy a Microsoft Dynamics 365 Talent: Core HR database to a sandbox environment.</span></span> <span data-ttu-id="9eeb5-114">Hvis du har et annet sandkassemiljø, kan du også kopiere databasen fra dette miljøet til et målrettet sandkassemiljø.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-114">If you have another sandbox environment, you can also copy the database from that environment to a targeted sandbox environment.</span></span> <span data-ttu-id="9eeb5-115">Hvis du vil ha mer informasjon,  kan du se:</span><span class="sxs-lookup"><span data-stu-id="9eeb5-115">For more information, see:</span></span>

- <span data-ttu-id="9eeb5-116">[Mer omfattende miljøbehandling](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) i Dynamics 365: 2019-frigivelsesbølge 2-planen</span><span class="sxs-lookup"><span data-stu-id="9eeb5-116">[Broader environment management](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/broader-environment-management) in the Dynamics 365: 2019 release wave 2 plan</span></span>

- <span data-ttu-id="9eeb5-117">[Kopiere en Core HR-forekomst](hr-copy-instance.md) i Talent-dokumentasjon</span><span class="sxs-lookup"><span data-stu-id="9eeb5-117">[Copy a Core HR instance](hr-copy-instance.md) in Talent documentation</span></span>

### <a name="common-data-service-integration-batch-jobs-arent-created-when-common-data-service-integration-is-enabled-388030"></a><span data-ttu-id="9eeb5-118">Common Data Service-partijobber for integrasjon blir ikke opprettet når Common Data Service-integrering er aktivert (388030)</span><span class="sxs-lookup"><span data-stu-id="9eeb5-118">Common Data Service integration batch jobs aren't created when Common Data Service integration is enabled (388030)</span></span>

<span data-ttu-id="9eeb5-119">Denne endringen vil opprette satsvise jobber for Common Data Service-integrering når den aktiveres.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-119">This change will create batch jobs for Common Data Service integration when it's enabled.</span></span>

### <a name="the-hcmpersonimageentity-doesnt-resize-the-person-image-when-uploaded-369469"></a><span data-ttu-id="9eeb5-120">HcmPersonImageEntity endrer ikke størrelse på personbildet når det lastes opp (369469)</span><span class="sxs-lookup"><span data-stu-id="9eeb5-120">The HcmPersonImageEntity doesn't resize the person image when uploaded (369469)</span></span>

<span data-ttu-id="9eeb5-121">Frigivelsen denne uken endrer hvordan bildestørrelser endres for bedre ytelse når de importeres ved hjelp av databehandling.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-121">This week's release changes how images are resized for better performance when imported through data management.</span></span>

### <a name="a-positions-available-for-assignment-date-can-be-earlier-than-the-activation-date-340103"></a><span data-ttu-id="9eeb5-122">En stilling som er tilgjengelig for tilordningsdatoen, kan være tidligere enn aktiveringsdatoen (340103)</span><span class="sxs-lookup"><span data-stu-id="9eeb5-122">A position's Available for assignment date can be earlier than the Activation date (340103)</span></span>

<span data-ttu-id="9eeb5-123">Med denne endringen vil det vises en advarsel hvis du velger en **Tilgjengelig for tilordningsdato** som er tidligere enn stillingens **aktiveringsdato**.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-123">With this change, a warning will appear if you select an **Available for assignment date** that's earlier than the position's **Activation date**.</span></span>

### <a name="cant-create-a-compensation-change-request-in-employee-self-service-for-step-based-plans-376872"></a><span data-ttu-id="9eeb5-124">Kan ikke opprette en kompensasjonsendringsforespørsel i ansattselvbetjening for trinnbaserte planer (376872)</span><span class="sxs-lookup"><span data-stu-id="9eeb5-124">Can't create a compensation change request in employee self-service for step-based plans (376872)</span></span>

<span data-ttu-id="9eeb5-125">Denne versjonen retter opp et problem når det bes om kompensasjonsendringer via ansattselvbetjening for trinnbaserte planer.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-125">This release corrects an issue when requesting compensation changes through employee self-service for step-based plans.</span></span> 

### <a name="reason-code-doesnt-sync-to-common-data-service-if-the-description-is-longer-than-30-characters-core-hr-allows-60-352682"></a><span data-ttu-id="9eeb5-126">Årsakskode synkroniseres ikke til Common Data Service hvis beskrivelsen er lengre enn 30 tegn, Core HR tillater 60 (352682)</span><span class="sxs-lookup"><span data-stu-id="9eeb5-126">Reason code doesn't sync to Common Data Service if the description is longer than 30 characters, Core HR allows 60 (352682)</span></span>

<span data-ttu-id="9eeb5-127">Med denne endringen blir årsakskoder med flere enn 30 tegn oppdatert i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-127">with this change, reason codes with more than 30 characters will be updated in Common Data Service.</span></span> <span data-ttu-id="9eeb5-128">Endringer som gjøres Common Data Service, vil også gjenspeiles i Talent.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-128">Changes made in Common Data Service will also be reflected back in Talent.</span></span>

### <a name="address-integration-from-talent-to-finance-and-operations-351961"></a><span data-ttu-id="9eeb5-129">Adresseintegrering fra Talent til Finance and Operations (351961)</span><span class="sxs-lookup"><span data-stu-id="9eeb5-129">Address integration from Talent to Finance and Operations (351961)</span></span>

<span data-ttu-id="9eeb5-130">Denne versjonen løser et problem der adresser som oppdateres i Talent, ikke ble oppdatert i Finance and Operations.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-130">This release fixes an issue where addresses updated in Talent weren't updating in Finance and Operations.</span></span> <span data-ttu-id="9eeb5-131">Endringer i adresseblokker blir nå oppdatert.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-131">Changes to address blocks will now update.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="9eeb5-132">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="9eeb5-132">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="9eeb5-133">Skrive ut prestasjonsvurderinger</span><span class="sxs-lookup"><span data-stu-id="9eeb5-133">Print performance reviews</span></span>

<span data-ttu-id="9eeb5-134">Se [Skrive ut prestasjonsvurderinger](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019-frigivelsesbølge 2-planen.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-134">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="9eeb5-135">Arbeidsområde for funksjonsbehandling</span><span class="sxs-lookup"><span data-stu-id="9eeb5-135">Feature management workspace</span></span>

<span data-ttu-id="9eeb5-136">Funksjoner legges til og oppdateres i hver versjon.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-136">Features are added and updated in every release.</span></span> <span data-ttu-id="9eeb5-137">Funksjonsbehandling-opplevelsen gir et arbeidsområde der du kan vise en liste over funksjoner som er levert i hver versjon.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-137">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="9eeb5-138">Nye funksjoner er deaktivert som standard.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-138">By default, new features are turned off.</span></span> <span data-ttu-id="9eeb5-139">Du kan bruke arbeidsområdet til å aktivere dem og vise dokumentasjonen for dem.</span><span class="sxs-lookup"><span data-stu-id="9eeb5-139">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="9eeb5-140">Hvis du vil ha mer informasjon om endringene som kommer med funksjonsbehandling, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="9eeb5-140">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
