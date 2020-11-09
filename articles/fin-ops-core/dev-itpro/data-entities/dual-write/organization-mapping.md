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
ms.custom: ''
ms.assetid: ''
ms.search.region: global
ms.search.industry: ''
ms.author: ramasri
ms.dyn365.ops.version: ''
ms.search.validFrom: 2019-07-15
ms.openlocfilehash: f502519ba419cb8fa322eb1d22f06d2b805f5f05
ms.sourcegitcommit: afc43699c0edc4ff2be310cb37add2ab586b64c0
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/14/2020
ms.locfileid: "4000740"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="f95b7-103">Organisasjonshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="f95b7-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f95b7-104">Fordi Dynamics 365 Finance er et finansielt system, er *organisasjon* et kjernekonsept, og systemoppsettet starter med konfigurasjonen av et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="f95b7-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="f95b7-105">Forretningsøkonomi kan deretter spores på organisasjonsnivå og også på et hvilket som helst nivå i organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f95b7-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="f95b7-106">Selv om Common Data Service ikke har konseptet med et organisasjonshierarki, har det noen løse konsepter, for eksempel totale salgsinntekter.</span><span class="sxs-lookup"><span data-stu-id="f95b7-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="f95b7-107">Som en del av Common Data Service-integreringen legges datastrukturen for organisasjonshierarkiet til i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f95b7-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="f95b7-108">Dataflyt</span><span class="sxs-lookup"><span data-stu-id="f95b7-108">Data flow</span></span>

<span data-ttu-id="f95b7-109">Et forretningsøkosystem som består av Finance and Operations-apper og Common Data Service, vil fortsatt ha et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="f95b7-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="f95b7-110">Dette organisasjonshierarkiet er bygd på Finance and Operations-apper, men det eksponeres i Common Data Service for informasjons- og utvidelsesformål.</span><span class="sxs-lookup"><span data-stu-id="f95b7-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="f95b7-111">Illustrasjonen nedenfor viser informasjon om organisasjonshierarkiet som vises i Common Data Service, som en énveis dataflyt fra Finance and Operations-apper til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f95b7-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Bilde av arkitektur](media/dual-write-data-flow.png)

<span data-ttu-id="f95b7-113">Enhetstilordninger for organisasjonshierarki er tilgjengelige for enveissynkronisering av data fra Finance and Operations-apper til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="f95b7-113">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

## <a name="templates"></a><span data-ttu-id="f95b7-114">Maler</span><span class="sxs-lookup"><span data-stu-id="f95b7-114">Templates</span></span>

<span data-ttu-id="f95b7-115">Produktinformasjonen inneholder all informasjonen som er knyttet til produktet og definisjonen, for eksempel produktdimensjonene eller sporings- og lagerdimensjonene.</span><span class="sxs-lookup"><span data-stu-id="f95b7-115">Product information contains all the information related to the product and its definition, such as the product dimensions or the tracking and storage dimensions.</span></span> <span data-ttu-id="f95b7-116">Som følgende tabell viser opprettes en samling enhetstilordning for å synkronisere produkter og beslektet informasjon.</span><span class="sxs-lookup"><span data-stu-id="f95b7-116">As the following table shows, a collection of entity maps is created to sync products and related information.</span></span>

<span data-ttu-id="f95b7-117">Finance and Operations-apper</span><span class="sxs-lookup"><span data-stu-id="f95b7-117">Finance and Operations apps</span></span> | <span data-ttu-id="f95b7-118">Andre Dynamics 365-apper</span><span class="sxs-lookup"><span data-stu-id="f95b7-118">Other Dynamics 365 apps</span></span> | <span data-ttu-id="f95b7-119">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="f95b7-119">Description</span></span>
-----------------------|--------------------------------|---
<span data-ttu-id="f95b7-120">Formål for organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="f95b7-120">Organization hierarchy purposes</span></span> | <span data-ttu-id="f95b7-121">msdyn_internalorganizationhierarchypurposes</span><span class="sxs-lookup"><span data-stu-id="f95b7-121">msdyn_internalorganizationhierarchypurposes</span></span> | <span data-ttu-id="f95b7-122">Denne malen gir enveis synkronisering av formålsenheten for organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f95b7-122">This template provides one-way synchronization of the Organization Hierarchy Purpose entity.</span></span>
<span data-ttu-id="f95b7-123">Type organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="f95b7-123">Organization hierarchy type</span></span> | <span data-ttu-id="f95b7-124">msdyn_internalorganizationhierarchytypes</span><span class="sxs-lookup"><span data-stu-id="f95b7-124">msdyn_internalorganizationhierarchytypes</span></span> | <span data-ttu-id="f95b7-125">Denne malen gir enveis synkronisering av typeenheten for organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f95b7-125">This template provides one-way synchronization of the Organization Hierarchy Type entity.</span></span>
<span data-ttu-id="f95b7-126">Organisasjonshierarki - publisert</span><span class="sxs-lookup"><span data-stu-id="f95b7-126">Organization hierarchy - published</span></span> | <span data-ttu-id="f95b7-127">msdyn_internalorganizationhierarchies</span><span class="sxs-lookup"><span data-stu-id="f95b7-127">msdyn_internalorganizationhierarchies</span></span> | <span data-ttu-id="f95b7-128">Denne malen gir enveis synkronisering av den publiserte enheten for organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="f95b7-128">This template provides one-way synchronization of the Organization Hierarchy Published entity.</span></span>
<span data-ttu-id="f95b7-129">Driftsenhet</span><span class="sxs-lookup"><span data-stu-id="f95b7-129">Operating unit</span></span> | <span data-ttu-id="f95b7-130">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="f95b7-130">msdyn_internalorganizations</span></span> |
<span data-ttu-id="f95b7-131">Juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="f95b7-131">Legal entities</span></span> | <span data-ttu-id="f95b7-132">msdyn_internalorganizations</span><span class="sxs-lookup"><span data-stu-id="f95b7-132">msdyn_internalorganizations</span></span> |
<span data-ttu-id="f95b7-133">Juridiske enheter</span><span class="sxs-lookup"><span data-stu-id="f95b7-133">Legal entities</span></span> | <span data-ttu-id="f95b7-134">cdm_companies</span><span class="sxs-lookup"><span data-stu-id="f95b7-134">cdm_companies</span></span> | <span data-ttu-id="f95b7-135">Gir toveis synkronisering av informasjon om juridisk enhet (firma).</span><span class="sxs-lookup"><span data-stu-id="f95b7-135">Provides bidirectional synchronization of legal entity (company) information.</span></span>

[!include [banner](../../includes/dual-write-symbols.md)]

[!include [Organization hierarchy purposes](includes/OrganizationHierarchyPurpose-msdyn-internalorganizationhierarchypurposes.md)]

[!include [Organization hierarchy type](includes/OrganizationHierarchyType-msdyn-internalorganizationhierarchytypes.md)]

[!include [Organization hierarchy - published](includes/OrganizationHierarchyPublished-msdyn-internalorganizationhierarchies.md)]

## <a name="internal-organization"></a><span data-ttu-id="f95b7-136">Intern organisasjon</span><span class="sxs-lookup"><span data-stu-id="f95b7-136">Internal Organization</span></span>

<span data-ttu-id="f95b7-137">Informasjon om intern organisasjon i Common Data Service kommer fra to enheter, **driftsenhet** og **juridiske enheter**.</span><span class="sxs-lookup"><span data-stu-id="f95b7-137">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

[!include [Operating unit](includes/OperatingUnit-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-msdyn-internalorganizations.md)]

[!include [Legal entities](includes/LegalEntities-Companies.md)]
