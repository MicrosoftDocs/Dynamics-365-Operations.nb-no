---
title: Organisasjonshierarki i Common Data Service
description: Dette emnet beskriver integreringen av organisasjonsdata mellom Finance and Operations-apper og Common Data Service.
author: RamaKrishnamoorthy
manager: AnnBe
ms.date: 07/15/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ''
audience: Application User, IT Pro
ms.reviewer: rhaertle
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: fbf7cc33d12fb54d2ff02acc46ba2e284b2a2b3f
ms.sourcegitcommit: 54baab2a04e5c534fc2d1fd67b67e23a152d4e57
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2020
ms.locfileid: "3019938"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="f702a-103">Organisasjonshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f702a-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

[!include [preview-banner](../../includes/preview-banner.md)]

<span data-ttu-id="f702a-104">Fordi Dynamics 365 Finance er et finansielt system, er *organisasjon* et kjernekonsept, og systemoppsettet starter med konfigurasjonen av et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="f702a-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="f702a-105">Forretningsøkonomi kan deretter spores på organisasjonsnivå og også på et hvilket som helst nivå i organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f702a-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="f702a-106">Selv om Common Data Service ikke har konseptet med et organisasjonshierarki, har det noen løse konsepter, for eksempel totale salgsinntekter.</span><span class="sxs-lookup"><span data-stu-id="f702a-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="f702a-107">Som en del av Common Data Service-integreringen legges datastrukturen for organisasjonshierarkiet til i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f702a-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="f702a-108">Dataflyt</span><span class="sxs-lookup"><span data-stu-id="f702a-108">Data flow</span></span>

<span data-ttu-id="f702a-109">Et forretningsøkosystem som består av Finance and Operations-apper og Common Data Service, vil fortsatt ha et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="f702a-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="f702a-110">Dette organisasjonshierarkiet er bygd på Finance and Operations-apper, men det eksponeres i Common Data Service for informasjons- og utvidelsesformål.</span><span class="sxs-lookup"><span data-stu-id="f702a-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="f702a-111">Illustrasjonen nedenfor viser informasjon om organisasjonshierarkiet som vises i Common Data Service, som en énveis dataflyt fra Finance and Operations-apper til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f702a-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Bilde av arkitektur](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="f702a-113">Maler</span><span class="sxs-lookup"><span data-stu-id="f702a-113">Templates</span></span>

<span data-ttu-id="f702a-114">Enhetstilordninger for organisasjonshierarki er tilgjengelige for enveissynkronisering av data fra Finance and Operations-apper til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f702a-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="f702a-115">Maler</span><span class="sxs-lookup"><span data-stu-id="f702a-115">Templates</span></span>

<span data-ttu-id="f702a-116">Produktinformasjonen inneholder all informasjonen som er knyttet til produktet og definisjonen, for eksempel produktdimensjonene eller sporings- og lagerdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="f702a-116">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="f702a-117">Som følgende tabell viser opprettes en samling enhetstilordning for å synkronisere produkter og beslektet informasjon.</span><span class="sxs-lookup"><span data-stu-id="f702a-117">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="f702a-118">Finance and Operations</span><span class="sxs-lookup"><span data-stu-id="f702a-118">Finance and Operations</span></span> | <span data-ttu-id="f702a-119">Andre Dynamics 365-apper</span><span class="sxs-lookup"><span data-stu-id="f702a-119">Other Dynamics 365 apps</span></span> | <span data-ttu-id="f702a-120">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f702a-120">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="f702a-121">Formål for organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="f702a-121">Organization hierarchy purposes</span></span> | <span data-ttu-id="f702a-122">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="f702a-122">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="f702a-123">Denne malen gir enveis synkronisering av formålsenheten for organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f702a-123">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="f702a-124">Type organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="f702a-124">Organization hierarchy type</span></span> | <span data-ttu-id="f702a-125">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="f702a-125">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="f702a-126">Denne malen gir enveis synkronisering av typeenheten for organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f702a-126">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="f702a-127">Organisasjonshierarki - publisert</span><span class="sxs-lookup"><span data-stu-id="f702a-127">Organization hierarchy - published</span></span> | <span data-ttu-id="f702a-128">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="f702a-128">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="f702a-129">Denne malen gir enveis synkronisering av den publiserte enheten for organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f702a-129">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="f702a-130">Driftsenhet</span><span class="sxs-lookup"><span data-stu-id="f702a-130">Operating unit</span></span> | <span data-ttu-id="f702a-131">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="f702a-131">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="f702a-132">Juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="f702a-132">Legal entities</span></span> | <span data-ttu-id="f702a-133">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="f702a-133">msdyn_internalorganizations</span></span> | 
<span data-ttu-id="f702a-134">Juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="f702a-134">Legal entities</span></span> | <span data-ttu-id="f702a-135">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="f702a-135">cdm_companies</span></span> | <span data-ttu-id="f702a-136">Gir toveis synkronisering av informasjon om juridisk enhet (firma).</span><span class="sxs-lookup"><span data-stu-id="f702a-136">Provides bidirectional synchronization of legal entity (company) information.</span></span>


[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="f702a-137">Intern organisasjon</span><span class="sxs-lookup"><span data-stu-id="f702a-137">Internal Organization</span></span>

<span data-ttu-id="f702a-138">Informasjon om intern organisasjon i Common Data Service kommer fra to enheter, **driftsenhet** og **juridiske enheter**.</span><span class="sxs-lookup"><span data-stu-id="f702a-138">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]

