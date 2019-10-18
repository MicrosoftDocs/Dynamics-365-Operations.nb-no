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
ms.openlocfilehash: fd159b38f69305dcaecb364ba0ccb3befabb3582
ms.sourcegitcommit: 3ba95d50b8262fa0f43d4faad76adac4d05eb3ea
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 09/27/2019
ms.locfileid: "2182031"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="96e06-103">Organisasjonshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="96e06-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="96e06-104">Fordi Dynamics 365 Finance er et finansielt system, er *organisasjon* et kjernekonsept, og systemoppsettet starter med konfigurasjonen av et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="96e06-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="96e06-105">Forretningsøkonomi kan deretter spores på organisasjonsnivå og også på et hvilket som helst nivå i organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="96e06-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="96e06-106">Selv om Common Data Service ikke har konseptet med et organisasjonshierarki, har det noen løse konsepter, for eksempel totale salgsinntekter.</span><span class="sxs-lookup"><span data-stu-id="96e06-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="96e06-107">Som en del av Common Data Service-integreringen legges datastrukturen for organisasjonshierarkiet til i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="96e06-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="96e06-108">Dataflyt</span><span class="sxs-lookup"><span data-stu-id="96e06-108">Data flow</span></span>

<span data-ttu-id="96e06-109">Et forretningsøkosystem som består av Finance and Operations-apper og Common Data Service, vil fortsatt ha et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="96e06-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="96e06-110">Dette organisasjonshierarkiet er bygd på Finance and Operations-apper, men det eksponeres i Common Data Service for informasjons- og utvidelsesformål.</span><span class="sxs-lookup"><span data-stu-id="96e06-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="96e06-111">Illustrasjonen nedenfor viser informasjon om organisasjonshierarkiet som vises i Common Data Service, som en énveis dataflyt fra Finance and Operations-apper til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="96e06-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Bilde av arkitektur](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="96e06-113">Maler</span><span class="sxs-lookup"><span data-stu-id="96e06-113">Templates</span></span>

<span data-ttu-id="96e06-114">Enhetstilordninger for organisasjonshierarki er tilgjengelige for enveissynkronisering av data fra Finance and Operations-apper til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="96e06-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="96e06-115">Formålet med internt organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="96e06-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="96e06-116">Denne malen gir enveissynkronisering av formålsenheten for organisasjonshierarkiet fra Finance and Operations til andre Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="96e06-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="96e06-117">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="96e06-117">Source field</span></span> | <span data-ttu-id="96e06-118">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="96e06-118">Map type</span></span> | <span data-ttu-id="96e06-119">Målfelt</span><span class="sxs-lookup"><span data-stu-id="96e06-119">Destination field</span></span>
---|---|---
<span data-ttu-id="96e06-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="96e06-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="96e06-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="96e06-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="96e06-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="96e06-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="96e06-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="96e06-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="96e06-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="96e06-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="96e06-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="96e06-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="96e06-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="96e06-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="96e06-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="96e06-127">msdyn\_immutable</span></span>
<span data-ttu-id="96e06-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="96e06-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="96e06-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="96e06-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="96e06-130">Intern organisasjonshierarkitype</span><span class="sxs-lookup"><span data-stu-id="96e06-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="96e06-131">Denne malen gir enveissynkronisering av typeenheten for organisasjonshierarkiet fra Finance and Operations til andre Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="96e06-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="96e06-132">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="96e06-132">Source field</span></span> | <span data-ttu-id="96e06-133">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="96e06-133">Map type</span></span> | <span data-ttu-id="96e06-134">Målfelt</span><span class="sxs-lookup"><span data-stu-id="96e06-134">Destination field</span></span>
---|---|---
<span data-ttu-id="96e06-135">NAVN</span><span class="sxs-lookup"><span data-stu-id="96e06-135">NAME</span></span> | \> | <span data-ttu-id="96e06-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="96e06-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="96e06-137">Internt organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="96e06-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="96e06-138">Denne malen gir enveissynkronisering av publisert enhet for organisasjonshierarkiet fra Finance and Operations til andre Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="96e06-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="96e06-139">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="96e06-139">Source field</span></span> | <span data-ttu-id="96e06-140">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="96e06-140">Map type</span></span> | <span data-ttu-id="96e06-141">Målfelt</span><span class="sxs-lookup"><span data-stu-id="96e06-141">Destination field</span></span>
---|---|---
<span data-ttu-id="96e06-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="96e06-142">VALIDTO</span></span> | \> | <span data-ttu-id="96e06-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="96e06-143">msdyn\_validto</span></span>
<span data-ttu-id="96e06-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="96e06-144">VALIDFROM</span></span> | \> | <span data-ttu-id="96e06-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="96e06-145">msdyn\_validfrom</span></span>
<span data-ttu-id="96e06-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="96e06-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="96e06-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="96e06-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="96e06-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="96e06-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="96e06-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="96e06-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="96e06-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="96e06-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="96e06-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="96e06-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="96e06-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="96e06-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="96e06-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="96e06-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="96e06-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="96e06-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="96e06-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="96e06-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="96e06-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="96e06-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="96e06-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="96e06-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="96e06-158">Intern organisasjon</span><span class="sxs-lookup"><span data-stu-id="96e06-158">Internal Organization</span></span>

<span data-ttu-id="96e06-159">Informasjon om intern organisasjon i Common Data Service kommer fra to enheter, **driftsenhet** og **juridiske enheter**.</span><span class="sxs-lookup"><span data-stu-id="96e06-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="96e06-160">Driftsenhet</span><span class="sxs-lookup"><span data-stu-id="96e06-160">Operating unit</span></span>

<span data-ttu-id="96e06-161">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="96e06-161">Source field</span></span> | <span data-ttu-id="96e06-162">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="96e06-162">Map type</span></span> | <span data-ttu-id="96e06-163">Målfelt</span><span class="sxs-lookup"><span data-stu-id="96e06-163">Destination field</span></span>
---|---|---
<span data-ttu-id="96e06-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="96e06-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="96e06-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="96e06-165">msdyn\_languageid</span></span>
<span data-ttu-id="96e06-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="96e06-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="96e06-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="96e06-167">msdyn\_namealias</span></span>
<span data-ttu-id="96e06-168">NAVN</span><span class="sxs-lookup"><span data-stu-id="96e06-168">NAME</span></span> | \> | <span data-ttu-id="96e06-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="96e06-169">msdyn\_name</span></span>
<span data-ttu-id="96e06-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="96e06-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="96e06-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="96e06-171">msdyn\_partynumber</span></span>
<span data-ttu-id="96e06-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="96e06-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="96e06-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="96e06-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="96e06-174">Juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="96e06-174">Legal entity</span></span>

<span data-ttu-id="96e06-175">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="96e06-175">Source field</span></span> | <span data-ttu-id="96e06-176">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="96e06-176">Map type</span></span> | <span data-ttu-id="96e06-177">Målfelt</span><span class="sxs-lookup"><span data-stu-id="96e06-177">Destination field</span></span>
---|---|---
<span data-ttu-id="96e06-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="96e06-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="96e06-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="96e06-179">msdyn\_namealias</span></span>
<span data-ttu-id="96e06-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="96e06-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="96e06-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="96e06-181">msdyn\_languageid</span></span>
<span data-ttu-id="96e06-182">NAVN</span><span class="sxs-lookup"><span data-stu-id="96e06-182">NAME</span></span> | \> | <span data-ttu-id="96e06-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="96e06-183">msdyn\_name</span></span>
<span data-ttu-id="96e06-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="96e06-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="96e06-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="96e06-185">msdyn\_partynumber</span></span>
<span data-ttu-id="96e06-186">none</span><span class="sxs-lookup"><span data-stu-id="96e06-186">none</span></span> | \>\> | <span data-ttu-id="96e06-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="96e06-187">msdyn\_type</span></span>
<span data-ttu-id="96e06-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="96e06-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="96e06-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="96e06-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="96e06-190">Bedrift</span><span class="sxs-lookup"><span data-stu-id="96e06-190">Company</span></span>

<span data-ttu-id="96e06-191">Gir toveissynkronisering av informasjon om juridisk enhet (firma) mellom Finance and Operations og andre Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="96e06-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="96e06-192">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="96e06-192">Source field</span></span> | <span data-ttu-id="96e06-193">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="96e06-193">Map type</span></span> | <span data-ttu-id="96e06-194">Målfelt</span><span class="sxs-lookup"><span data-stu-id="96e06-194">Destination field</span></span>
---|---|---
<span data-ttu-id="96e06-195">NAVN</span><span class="sxs-lookup"><span data-stu-id="96e06-195">NAME</span></span> | = | <span data-ttu-id="96e06-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="96e06-196">cdm\_name</span></span>
<span data-ttu-id="96e06-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="96e06-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="96e06-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="96e06-198">cdm\_companycode</span></span>
