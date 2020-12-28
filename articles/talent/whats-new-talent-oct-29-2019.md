---
title: Hva er nytt eller endret i Dynamics 365 Talent (29. oktober 2019)
description: Dette emnet beskriver funksjoner som enten er nye eller endret i Microsoft Dynamics 365 Talent.
author: Darinkramer
manager: AnnBe
ms.date: 10/29/2019
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
ms.search.validFrom: 2019-10-29
ms.dyn365.ops.version: Talent
ms.openlocfilehash: 09d53c82b4244f20d0d7f301691b01263258a32f
ms.sourcegitcommit: e89bb3e5420a6ece84f4e80c11e360b4a042f59d
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/17/2020
ms.locfileid: "4529690"
---
# <a name="whats-new-or-changed-in-dynamics-365-talent-october-29-2019"></a><span data-ttu-id="c2d36-103">Hva er nytt eller endret i Dynamics 365 Talent (29. oktober 2019)</span><span class="sxs-lookup"><span data-stu-id="c2d36-103">What's new or changed in Dynamics 365 Talent (October 29, 2019)</span></span>

[!include [rename-banner](~/includes/cc-data-platform-banner.md)]

<span data-ttu-id="c2d36-104">Dette emnet beskriver funksjoner som enten er nye eller endret i Dynamics 365 Talent.</span><span class="sxs-lookup"><span data-stu-id="c2d36-104">This topic describes features that are either new or changed in Dynamics 365 Talent.</span></span>

## <a name="changes-in-attract"></a><span data-ttu-id="c2d36-105">Endringer i Attract</span><span class="sxs-lookup"><span data-stu-id="c2d36-105">Changes in Attract</span></span>

<span data-ttu-id="c2d36-106">Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Attract.</span><span class="sxs-lookup"><span data-stu-id="c2d36-106">This release includes minor bug fixes for Dynamics 365 Talent: Attract.</span></span>

## <a name="changes-in-onboard"></a><span data-ttu-id="c2d36-107">Endringer i Onboard</span><span class="sxs-lookup"><span data-stu-id="c2d36-107">Changes in Onboard</span></span>

<span data-ttu-id="c2d36-108">Denne versjonen inneholder mindre feilrettinger for Dynamics 365 Talent: Onboard.</span><span class="sxs-lookup"><span data-stu-id="c2d36-108">This release includes minor bug fixes for Dynamics 365 Talent: Onboard.</span></span>

## <a name="changes-in-core-hr"></a><span data-ttu-id="c2d36-109">Endringer i Core HR</span><span class="sxs-lookup"><span data-stu-id="c2d36-109">Changes in Core HR</span></span>

<span data-ttu-id="c2d36-110">Endringer som er beskrevet i denne delen, gjelder build nummer 8.1.2586.</span><span class="sxs-lookup"><span data-stu-id="c2d36-110">Changes described in this section apply to build number 8.1.2586.</span></span> <span data-ttu-id="c2d36-111">Tallene i parentes i noen overskrifter refererer til støttenumre i Microsoft Dynamics Lifecycle Services (LCS).</span><span class="sxs-lookup"><span data-stu-id="c2d36-111">The numbers in parentheses in some headings refer to support numbers in Microsoft Dynamics Lifecycle Services (LCS).</span></span>

### <a name="delete-parties-with-no-roles-should-be-on-by-default-371233"></a><span data-ttu-id="c2d36-112">Slett parter uten roller skal være aktivert som standard (371233)</span><span class="sxs-lookup"><span data-stu-id="c2d36-112">Delete parties with no roles should be on by default (371233)</span></span>

<span data-ttu-id="c2d36-113">Når du klargjør et nytt miljø i Talent, er **Slett parter uten roller** aktivert som standard.</span><span class="sxs-lookup"><span data-stu-id="c2d36-113">When you provision a new environment in Talent, **Delete parties if no roles exist** is turned on by default.</span></span> <span data-ttu-id="c2d36-114">Når du sletter en arbeider, blir ikke parten som er tilknyttet arbeideren, fjernet med mindre denne innstillingen er aktivert.</span><span class="sxs-lookup"><span data-stu-id="c2d36-114">When you delete a worker, the party associated with the worker is not removed unless this setting is on.</span></span> <span data-ttu-id="c2d36-115">Denne endringen begrenser like poster i den globale adresseboken når du har behov for å importere, endre eller importere arbeidere på nytt.</span><span class="sxs-lookup"><span data-stu-id="c2d36-115">This change limits duplicate records in the global address book when you need to import, change, or reimport workers.</span></span>

### <a name="draft-and-cancelled-leave-requests-should-be-allowed-to-be-deleted-in-common-data-service-376999"></a><span data-ttu-id="c2d36-116">Utkast og annullerte permisjonsforespørsler må kunne slettes i Common Data Service (376999)</span><span class="sxs-lookup"><span data-stu-id="c2d36-116">Draft and cancelled leave requests should be allowed to be deleted in Common Data Service (376999)</span></span>

<span data-ttu-id="c2d36-117">Med denne endringen kan du nå slette permisjonsforespørsler med statusen **utkast** eller **avbrutt** i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="c2d36-117">With this change, you can now delete leave requests with a status of **Draft** or **Cancelled** in Common Data Service.</span></span>

### <a name="additional-list-values-in-custom-fields-arent-reflected-in-common-data-service-after-clicking-apply-on-the-custom-fields-form-379599"></a><span data-ttu-id="c2d36-118">Flere listeverdier i egendefinerte felt gjenspeiles ikke i Common Data Service når du klikker Bruk på egendefinerte felt-skjemaet (379599)</span><span class="sxs-lookup"><span data-stu-id="c2d36-118">Additional list values in custom fields aren't reflected in Common Data Service after clicking Apply on the Custom fields form (379599)</span></span>

<span data-ttu-id="c2d36-119">Når du legger til nye listeverdier i et eksisterende egendefinert felt som allerede er synkronisert med Common Data Service, er de nå tilgjengelige i Common Data Service etter at du har brukt endringer i **Egendefinerte felt**-skjemaet.</span><span class="sxs-lookup"><span data-stu-id="c2d36-119">When you add new list values to an existing custom field that has already synchronized with Common Data Service, they're now available in Common Data Serivce after you apply your changes in the **Custom fields** form.</span></span>

### <a name="apply-onboarding-checklists-across-legal-entities-when-more-than-one-employment-exists-371270"></a><span data-ttu-id="c2d36-120">Bruk sjekklister for jobbintroduksjon på tvers av juridiske enheter når det finnes mer enn én ansettelse (371270)</span><span class="sxs-lookup"><span data-stu-id="c2d36-120">Apply onboarding checklists across legal entities when more than one employment exists (371270)</span></span>

<span data-ttu-id="c2d36-121">I denne ukens frigivelse kan du bruke sjekklister på ansatte med mer enn ett ansettelsesforhold i **Arbeider-skjema > Sjekklister**.</span><span class="sxs-lookup"><span data-stu-id="c2d36-121">In this week's release, you can apply checklists to employees with more than one employment in **Worker form > Checklists**.</span></span>

### <a name="benefits-open-enrollment-preview-feature-has-been-removed"></a><span data-ttu-id="c2d36-122">Åpen registrering for fordeler fra offentlig forhåndsvisning er fjernet</span><span class="sxs-lookup"><span data-stu-id="c2d36-122">Benefits open enrollment preview feature has been removed</span></span>

<span data-ttu-id="c2d36-123">I forbindelse med vår kunngjøring i blogginnlegget [Strategiske investeringene i Core HR gir til store driftsfordeler](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) har Microsoft fjernet funksjonen for åpen registrering av fordeler fra den offentlige forhåndsvisningen.</span><span class="sxs-lookup"><span data-stu-id="c2d36-123">In conjunction with our announcement in the [Strategic investments in core HR drive operational excellence](https://cloudblogs.microsoft.com/dynamics365/bdm/2019/10/02/strategic-investments-in-core-hr-drive-operational-excellence) blog post, Microsoft has removed the benefits open enrollment feature from public preview.</span></span> <span data-ttu-id="c2d36-124">Ny funksjonalitet vil bli utgitt i fremtiden.</span><span class="sxs-lookup"><span data-stu-id="c2d36-124">New functionality will be released in the future.</span></span> <span data-ttu-id="c2d36-125">Produksjonsbruk av funksjonen for åpen registrering for fordeler støttes ikke.</span><span class="sxs-lookup"><span data-stu-id="c2d36-125">Production use of the benefits open enrollment feature isn't be supported.</span></span>

## <a name="coming-soon"></a><span data-ttu-id="c2d36-126">Kommer snart</span><span class="sxs-lookup"><span data-stu-id="c2d36-126">Coming soon</span></span>

### <a name="print-performance-reviews"></a><span data-ttu-id="c2d36-127">Skrive ut prestasjonsvurderinger</span><span class="sxs-lookup"><span data-stu-id="c2d36-127">Print performance reviews</span></span>

<span data-ttu-id="c2d36-128">Se [Skrive ut prestasjonsvurderinger](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) i Dynamics 365: 2019-frigivelsesbølge 2-planen.</span><span class="sxs-lookup"><span data-stu-id="c2d36-128">See [Print performance reviews](https://docs.microsoft.com/dynamics365-release-plan/2019wave2/dynamics365-talent/print-performance-reviews) in the Dynamics 365: 2019 release wave 2 plan.</span></span>

### <a name="feature-management-workspace"></a><span data-ttu-id="c2d36-129">Arbeidsområde for funksjonsbehandling</span><span class="sxs-lookup"><span data-stu-id="c2d36-129">Feature management workspace</span></span>

<span data-ttu-id="c2d36-130">Funksjoner legges til og oppdateres i hver versjon.</span><span class="sxs-lookup"><span data-stu-id="c2d36-130">Features are added and updated in every release.</span></span> <span data-ttu-id="c2d36-131">Funksjonsbehandling-opplevelsen gir et arbeidsområde der du kan vise en liste over funksjoner som er levert i hver versjon.</span><span class="sxs-lookup"><span data-stu-id="c2d36-131">The feature management experience provides a workspace where you can view a list of features that have been delivered in each release.</span></span> <span data-ttu-id="c2d36-132">Nye funksjoner er deaktivert som standard.</span><span class="sxs-lookup"><span data-stu-id="c2d36-132">By default, new features are turned off.</span></span> <span data-ttu-id="c2d36-133">Du kan bruke arbeidsområdet til å aktivere dem og vise dokumentasjonen for dem.</span><span class="sxs-lookup"><span data-stu-id="c2d36-133">You can use the workspace to turn them on and view the documentation for them.</span></span>

<span data-ttu-id="c2d36-134">Hvis du vil ha mer informasjon om endringene som kommer med funksjonsbehandling, kan du se [Oversikt over funksjonsbehandling](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span><span class="sxs-lookup"><span data-stu-id="c2d36-134">To learn more about the changes coming with feature management, see [Feature management overview](https://docs.microsoft.com/dynamics365/fin-ops-core/fin-ops/get-started/feature-management/feature-management-overview).</span></span>
