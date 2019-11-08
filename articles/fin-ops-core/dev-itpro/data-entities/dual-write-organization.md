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
ms.openlocfilehash: 9a12ab249129dce24cdca5e29d737fa9f68c0eac
ms.sourcegitcommit: 6e0909e95f38b7487a4b7f68cc62b723f8b59bd4
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2019
ms.locfileid: "2572455"
---
# <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="bbda8-103">Organisasjonshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="bbda8-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="bbda8-104">Fordi Dynamics 365 Finance er et finansielt system, er *organisasjon* et kjernekonsept, og systemoppsettet starter med konfigurasjonen av et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="bbda8-104">Because Dynamics 365 Finance is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="bbda8-105">Forretningsøkonomi kan deretter spores på organisasjonsnivå og også på et hvilket som helst nivå i organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="bbda8-105">Business financials can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="bbda8-106">Selv om Common Data Service ikke har konseptet med et organisasjonshierarki, har det noen løse konsepter, for eksempel totale salgsinntekter.</span><span class="sxs-lookup"><span data-stu-id="bbda8-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="bbda8-107">Som en del av Common Data Service-integreringen legges datastrukturen for organisasjonshierarkiet til i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="bbda8-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="bbda8-108">Dataflyt</span><span class="sxs-lookup"><span data-stu-id="bbda8-108">Data flow</span></span>

<span data-ttu-id="bbda8-109">Et forretningsøkosystem som består av Finance and Operations-apper og Common Data Service, vil fortsatt ha et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="bbda8-109">A business ecosystem that consists of Finance and Operations apps and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="bbda8-110">Dette organisasjonshierarkiet er bygd på Finance and Operations-apper, men det eksponeres i Common Data Service for informasjons- og utvidelsesformål.</span><span class="sxs-lookup"><span data-stu-id="bbda8-110">This organization hierarchy is built on Finance and Operations apps, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="bbda8-111">Illustrasjonen nedenfor viser informasjon om organisasjonshierarkiet som vises i Common Data Service, som en énveis dataflyt fra Finance and Operations-apper til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="bbda8-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations apps to Common Data Service.</span></span>

![Bilde av arkitektur](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="bbda8-113">Maler</span><span class="sxs-lookup"><span data-stu-id="bbda8-113">Templates</span></span>

<span data-ttu-id="bbda8-114">Enhetstilordninger for organisasjonshierarki er tilgjengelige for enveissynkronisering av data fra Finance and Operations-apper til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="bbda8-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations apps to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="bbda8-115">Formålet med internt organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="bbda8-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="bbda8-116">Denne malen gir enveissynkronisering av formålsenheten for organisasjonshierarkiet fra Finance and Operations til andre Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="bbda8-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="bbda8-117">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="bbda8-117">Source field</span></span> | <span data-ttu-id="bbda8-118">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="bbda8-118">Map type</span></span> | <span data-ttu-id="bbda8-119">Målfelt</span><span class="sxs-lookup"><span data-stu-id="bbda8-119">Destination field</span></span>
---|---|---
<span data-ttu-id="bbda8-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="bbda8-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="bbda8-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="bbda8-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="bbda8-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="bbda8-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="bbda8-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="bbda8-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="bbda8-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="bbda8-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="bbda8-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="bbda8-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="bbda8-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="bbda8-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="bbda8-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="bbda8-127">msdyn\_immutable</span></span>
<span data-ttu-id="bbda8-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="bbda8-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="bbda8-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="bbda8-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="bbda8-130">Intern organisasjonshierarkitype</span><span class="sxs-lookup"><span data-stu-id="bbda8-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="bbda8-131">Denne malen gir enveissynkronisering av typeenheten for organisasjonshierarkiet fra Finance and Operations til andre Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="bbda8-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="bbda8-132">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="bbda8-132">Source field</span></span> | <span data-ttu-id="bbda8-133">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="bbda8-133">Map type</span></span> | <span data-ttu-id="bbda8-134">Målfelt</span><span class="sxs-lookup"><span data-stu-id="bbda8-134">Destination field</span></span>
---|---|---
<span data-ttu-id="bbda8-135">NAVN</span><span class="sxs-lookup"><span data-stu-id="bbda8-135">NAME</span></span> | \> | <span data-ttu-id="bbda8-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="bbda8-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="bbda8-137">Internt organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="bbda8-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="bbda8-138">Denne malen gir enveissynkronisering av publisert enhet for organisasjonshierarkiet fra Finance and Operations til andre Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="bbda8-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="bbda8-139">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="bbda8-139">Source field</span></span> | <span data-ttu-id="bbda8-140">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="bbda8-140">Map type</span></span> | <span data-ttu-id="bbda8-141">Målfelt</span><span class="sxs-lookup"><span data-stu-id="bbda8-141">Destination field</span></span>
---|---|---
<span data-ttu-id="bbda8-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="bbda8-142">VALIDTO</span></span> | \> | <span data-ttu-id="bbda8-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="bbda8-143">msdyn\_validto</span></span>
<span data-ttu-id="bbda8-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="bbda8-144">VALIDFROM</span></span> | \> | <span data-ttu-id="bbda8-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="bbda8-145">msdyn\_validfrom</span></span>
<span data-ttu-id="bbda8-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="bbda8-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="bbda8-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="bbda8-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="bbda8-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="bbda8-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="bbda8-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="bbda8-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="bbda8-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="bbda8-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="bbda8-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="bbda8-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="bbda8-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="bbda8-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="bbda8-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="bbda8-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="bbda8-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="bbda8-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="bbda8-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="bbda8-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="bbda8-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="bbda8-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="bbda8-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="bbda8-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="bbda8-158">Intern organisasjon</span><span class="sxs-lookup"><span data-stu-id="bbda8-158">Internal Organization</span></span>

<span data-ttu-id="bbda8-159">Informasjon om intern organisasjon i Common Data Service kommer fra to enheter, **driftsenhet** og **juridiske enheter**.</span><span class="sxs-lookup"><span data-stu-id="bbda8-159">Internal organization information in Common Data Service comes from two entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="bbda8-160">Driftsenhet</span><span class="sxs-lookup"><span data-stu-id="bbda8-160">Operating unit</span></span>

<span data-ttu-id="bbda8-161">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="bbda8-161">Source field</span></span> | <span data-ttu-id="bbda8-162">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="bbda8-162">Map type</span></span> | <span data-ttu-id="bbda8-163">Målfelt</span><span class="sxs-lookup"><span data-stu-id="bbda8-163">Destination field</span></span>
---|---|---
<span data-ttu-id="bbda8-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="bbda8-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="bbda8-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="bbda8-165">msdyn\_languageid</span></span>
<span data-ttu-id="bbda8-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="bbda8-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="bbda8-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="bbda8-167">msdyn\_namealias</span></span>
<span data-ttu-id="bbda8-168">NAVN</span><span class="sxs-lookup"><span data-stu-id="bbda8-168">NAME</span></span> | \> | <span data-ttu-id="bbda8-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="bbda8-169">msdyn\_name</span></span>
<span data-ttu-id="bbda8-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="bbda8-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="bbda8-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="bbda8-171">msdyn\_partynumber</span></span>
<span data-ttu-id="bbda8-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="bbda8-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="bbda8-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="bbda8-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="bbda8-174">Juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="bbda8-174">Legal entity</span></span>

<span data-ttu-id="bbda8-175">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="bbda8-175">Source field</span></span> | <span data-ttu-id="bbda8-176">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="bbda8-176">Map type</span></span> | <span data-ttu-id="bbda8-177">Målfelt</span><span class="sxs-lookup"><span data-stu-id="bbda8-177">Destination field</span></span>
---|---|---
<span data-ttu-id="bbda8-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="bbda8-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="bbda8-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="bbda8-179">msdyn\_namealias</span></span>
<span data-ttu-id="bbda8-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="bbda8-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="bbda8-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="bbda8-181">msdyn\_languageid</span></span>
<span data-ttu-id="bbda8-182">NAVN</span><span class="sxs-lookup"><span data-stu-id="bbda8-182">NAME</span></span> | \> | <span data-ttu-id="bbda8-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="bbda8-183">msdyn\_name</span></span>
<span data-ttu-id="bbda8-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="bbda8-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="bbda8-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="bbda8-185">msdyn\_partynumber</span></span>
<span data-ttu-id="bbda8-186">none</span><span class="sxs-lookup"><span data-stu-id="bbda8-186">none</span></span> | \>\> | <span data-ttu-id="bbda8-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="bbda8-187">msdyn\_type</span></span>
<span data-ttu-id="bbda8-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="bbda8-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="bbda8-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="bbda8-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="bbda8-190">Bedrift</span><span class="sxs-lookup"><span data-stu-id="bbda8-190">Company</span></span>

<span data-ttu-id="bbda8-191">Gir toveissynkronisering av informasjon om juridisk enhet (firma) mellom Finance and Operations og andre Dynamics 365-apper.</span><span class="sxs-lookup"><span data-stu-id="bbda8-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and other Dynamics 365 apps.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="bbda8-192">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="bbda8-192">Source field</span></span> | <span data-ttu-id="bbda8-193">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="bbda8-193">Map type</span></span> | <span data-ttu-id="bbda8-194">Målfelt</span><span class="sxs-lookup"><span data-stu-id="bbda8-194">Destination field</span></span>
---|---|---
<span data-ttu-id="bbda8-195">NAVN</span><span class="sxs-lookup"><span data-stu-id="bbda8-195">NAME</span></span> | = | <span data-ttu-id="bbda8-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="bbda8-196">cdm\_name</span></span>
<span data-ttu-id="bbda8-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="bbda8-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="bbda8-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="bbda8-198">cdm\_companycode</span></span>
