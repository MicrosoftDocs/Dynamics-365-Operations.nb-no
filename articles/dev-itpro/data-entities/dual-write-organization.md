---
title: Organisasjonshierarki i Common Data Service
description: Dette emnet beskriver integreringen av organisasjonsdata mellom Finance and Operations og Common Data Service.
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
ms.openlocfilehash: ca2ac0f9dbb8544b12f23a271423a43b0e601272
ms.sourcegitcommit: 02c223b44ac7196df675afac61c6783f467d1983
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 07/24/2019
ms.locfileid: "1789228"
---
## <a name="organization-hierarchy-in-common-data-service"></a><span data-ttu-id="6adfb-103">Organisasjonshierarki i Common Data Service</span><span class="sxs-lookup"><span data-stu-id="6adfb-103">Organization hierarchy in Common Data Service</span></span>

[!include [banner](../includes/banner.md)]

[!include [preview](../includes/preview-banner.md)]

<span data-ttu-id="6adfb-104">Fordi Microsoft Dynamics 365 for Finance and Operations er et finansielt system, er *organisasjon* et kjernekonsept, og systemoppsettet starter med konfigurasjonen av et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="6adfb-104">Because Microsoft Dynamics 365 for Finance and Operations is a financial system, *organization* is a core concept, and system setup starts with the configuration of an organization hierarchy.</span></span> <span data-ttu-id="6adfb-105">Forretningsøkonomi og -operasjoner kan deretter spores på organisasjonsnivå og også på et hvilket som helst nivå i organisasjonshierarkiet.</span><span class="sxs-lookup"><span data-stu-id="6adfb-105">Business financials and operations can then be tracked at the organization level and also at any level in the organization hierarchy.</span></span>

<span data-ttu-id="6adfb-106">Selv om Common Data Service ikke har konseptet med et organisasjonshierarki, har det noen løse konsepter, for eksempel totale salgsinntekter.</span><span class="sxs-lookup"><span data-stu-id="6adfb-106">Although Common Data Service doesn't have the concept of an organization hierarchy, it does have a few loose concepts, such as total sales revenue.</span></span> <span data-ttu-id="6adfb-107">Som en del av Common Data Service-integreringen legges datastrukturen for organisasjonshierarkiet til i Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6adfb-107">As part of Common Data Service integration, the organization hierarchy data structure is added to Common Data Service.</span></span>

## <a name="data-flow"></a><span data-ttu-id="6adfb-108">Dataflyt</span><span class="sxs-lookup"><span data-stu-id="6adfb-108">Data flow</span></span>

<span data-ttu-id="6adfb-109">Et forretningsøkosystem som består av Finance and Operations og Common Data Service, vil fortsatt ha et organisasjonshierarki.</span><span class="sxs-lookup"><span data-stu-id="6adfb-109">A business ecosystem that consists of Finance and Operations and Common Data Service will continue to have an organization hierarchy.</span></span> <span data-ttu-id="6adfb-110">Dette organisasjonshierarkiet er bygd på Finance and Operations, men det eksponeres i Common Data Service for informasjons- og utvidelsesformål.</span><span class="sxs-lookup"><span data-stu-id="6adfb-110">This organization hierarchy is built on Finance and Operations, but it's exposed in Common Data Service for informational and extensibility purposes.</span></span> <span data-ttu-id="6adfb-111">Illustrasjonen nedenfor viser informasjon om organisasjonshierarkiet som vises i Common Data Service, som en énveis dataflyt fra Finance and Operations til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6adfb-111">The following illustration shows the organization hierarchy information that is exposed in Common Data Service as a one-way data flow from Finance and Operations to Common Data Service.</span></span>

![Bilde av arkitektur](media/dual-write-data-flow.png)

## <a name="templates"></a><span data-ttu-id="6adfb-113">Maler</span><span class="sxs-lookup"><span data-stu-id="6adfb-113">Templates</span></span>

<span data-ttu-id="6adfb-114">Enhetstilordninger for organisasjonshierarki er tilgjengelige for enveissynkronisering av data fra Finance and Operations til Common Data Service.</span><span class="sxs-lookup"><span data-stu-id="6adfb-114">Organization hierarchy entity maps are available for one-way synchronization of data from Finance and Operations to Common Data Service.</span></span>

[!include [banner](../includes/dual-write-symbols.md)]

## <a name="internal-organization-hierarchy-purpose"></a><span data-ttu-id="6adfb-115">Formålet med internt organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="6adfb-115">Internal Organization Hierarchy Purpose</span></span>

<span data-ttu-id="6adfb-116">Denne malen gir enveissynkronisering av formålsenheten for organisasjonshierarkiet fra Finance and Operations til Dynamics 365 for Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="6adfb-116">This template provides one-way synchronization of the Organization Hierarchy Purpose entity from Finance and Operations to Dynamics 365 for Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-purpose.png) -->

<span data-ttu-id="6adfb-117">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="6adfb-117">Source field</span></span> | <span data-ttu-id="6adfb-118">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="6adfb-118">Map type</span></span> | <span data-ttu-id="6adfb-119">Målfelt</span><span class="sxs-lookup"><span data-stu-id="6adfb-119">Destination field</span></span>
---|---|---
<span data-ttu-id="6adfb-120">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="6adfb-120">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="6adfb-121">msdyn\_hierarchypurposetypename</span><span class="sxs-lookup"><span data-stu-id="6adfb-121">msdyn\_hierarchypurposetypename</span></span>
<span data-ttu-id="6adfb-122">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="6adfb-122">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="6adfb-123">msdyn\_hierarchytype.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="6adfb-123">msdyn\_hierarchytype.msdyn\_name</span></span>
<span data-ttu-id="6adfb-124">HIERARCHYPURPOSE</span><span class="sxs-lookup"><span data-stu-id="6adfb-124">HIERARCHYPURPOSE</span></span> | \>\> | <span data-ttu-id="6adfb-125">msdyn\_hierarchypurpose</span><span class="sxs-lookup"><span data-stu-id="6adfb-125">msdyn\_hierarchypurpose</span></span>
<span data-ttu-id="6adfb-126">IMMUTABLE</span><span class="sxs-lookup"><span data-stu-id="6adfb-126">IMMUTABLE</span></span> | \>\> | <span data-ttu-id="6adfb-127">msdyn\_immutable</span><span class="sxs-lookup"><span data-stu-id="6adfb-127">msdyn\_immutable</span></span>
<span data-ttu-id="6adfb-128">SETASDEFAULT</span><span class="sxs-lookup"><span data-stu-id="6adfb-128">SETASDEFAULT</span></span> | \>\> | <span data-ttu-id="6adfb-129">msdyn\_setasdefault</span><span class="sxs-lookup"><span data-stu-id="6adfb-129">msdyn\_setasdefault</span></span>

## <a name="internal-organization-hierarchy-type"></a><span data-ttu-id="6adfb-130">Intern organisasjonshierarkitype</span><span class="sxs-lookup"><span data-stu-id="6adfb-130">Internal Organization Hierarchy Type</span></span>

<span data-ttu-id="6adfb-131">Denne malen gir enveissynkronisering av typeenheten for organisasjonshierarkiet fra Finance and Operations til Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="6adfb-131">Tihs template provides one-way synchronization of the Organization Hierarchy Type entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-type.png) -->

<span data-ttu-id="6adfb-132">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="6adfb-132">Source field</span></span> | <span data-ttu-id="6adfb-133">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="6adfb-133">Map type</span></span> | <span data-ttu-id="6adfb-134">Målfelt</span><span class="sxs-lookup"><span data-stu-id="6adfb-134">Destination field</span></span>
---|---|---
<span data-ttu-id="6adfb-135">NAVN</span><span class="sxs-lookup"><span data-stu-id="6adfb-135">NAME</span></span> | \> | <span data-ttu-id="6adfb-136">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="6adfb-136">msdyn\_name</span></span>

## <a name="internal-organization-hierarchy"></a><span data-ttu-id="6adfb-137">Internt organisasjonshierarki</span><span class="sxs-lookup"><span data-stu-id="6adfb-137">Internal Organization Hierarchy</span></span>

<span data-ttu-id="6adfb-138">Denne malen gir enveissynkronisering av den publiserte enheten for organisasjonshierarkiet fra Finance and Operations til Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="6adfb-138">This template provides one-way synchronization of the Organization Hierarchy Published entity from Finance and Operations to Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-organization.png) -->

<span data-ttu-id="6adfb-139">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="6adfb-139">Source field</span></span> | <span data-ttu-id="6adfb-140">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="6adfb-140">Map type</span></span> | <span data-ttu-id="6adfb-141">Målfelt</span><span class="sxs-lookup"><span data-stu-id="6adfb-141">Destination field</span></span>
---|---|---
<span data-ttu-id="6adfb-142">VALIDTO</span><span class="sxs-lookup"><span data-stu-id="6adfb-142">VALIDTO</span></span> | \> | <span data-ttu-id="6adfb-143">msdyn\_validto</span><span class="sxs-lookup"><span data-stu-id="6adfb-143">msdyn\_validto</span></span>
<span data-ttu-id="6adfb-144">VALIDFROM</span><span class="sxs-lookup"><span data-stu-id="6adfb-144">VALIDFROM</span></span> | \> | <span data-ttu-id="6adfb-145">msdyn\_validfrom</span><span class="sxs-lookup"><span data-stu-id="6adfb-145">msdyn\_validfrom</span></span>
<span data-ttu-id="6adfb-146">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="6adfb-146">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="6adfb-147">msdyn\_hierarchytypename</span><span class="sxs-lookup"><span data-stu-id="6adfb-147">msdyn\_hierarchytypename</span></span>
<span data-ttu-id="6adfb-148">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="6adfb-148">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="6adfb-149">msdyn\_parentpartyid</span><span class="sxs-lookup"><span data-stu-id="6adfb-149">msdyn\_parentpartyid</span></span>
<span data-ttu-id="6adfb-150">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="6adfb-150">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="6adfb-151">msdyn\_childpartyid</span><span class="sxs-lookup"><span data-stu-id="6adfb-151">msdyn\_childpartyid</span></span>
<span data-ttu-id="6adfb-152">HIERARCHYTYPE</span><span class="sxs-lookup"><span data-stu-id="6adfb-152">HIERARCHYTYPE</span></span> | \> | <span data-ttu-id="6adfb-153">msdyn\_hierarchytypeid.msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="6adfb-153">msdyn\_hierarchytypeid.msdyn\_name</span></span>
<span data-ttu-id="6adfb-154">CHILDORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="6adfb-154">CHILDORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="6adfb-155">msdyn\_childid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="6adfb-155">msdyn\_childid.msdyn\_partynumber</span></span>
<span data-ttu-id="6adfb-156">PARENTORGANIZATIONPARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="6adfb-156">PARENTORGANIZATIONPARTYNUMBER</span></span> | \> | <span data-ttu-id="6adfb-157">msdyn\_parentid.msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="6adfb-157">msdyn\_parentid.msdyn\_partynumber</span></span>

## <a name="internal-organization"></a><span data-ttu-id="6adfb-158">Intern organisasjon</span><span class="sxs-lookup"><span data-stu-id="6adfb-158">Internal Organization</span></span>

<span data-ttu-id="6adfb-159">Informasjon om intern organisasjon i Common Data Service kommer fra to Finance and Operations-enheter, **driftsenhet** og **juridiske enheter**.</span><span class="sxs-lookup"><span data-stu-id="6adfb-159">Internal organization information in Common Data Service comes from two Finance and Operations entities, **operating unit** and **legal entities**.</span></span>

<!-- ![architecture image](media/dual-write-operating-unit.png) -->

<!-- ![architecture image](media/dual-write-legal-entities.png) -->

### <a name="operating-unit"></a><span data-ttu-id="6adfb-160">Driftsenhet</span><span class="sxs-lookup"><span data-stu-id="6adfb-160">Operating unit</span></span>

<span data-ttu-id="6adfb-161">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="6adfb-161">Source field</span></span> | <span data-ttu-id="6adfb-162">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="6adfb-162">Map type</span></span> | <span data-ttu-id="6adfb-163">Målfelt</span><span class="sxs-lookup"><span data-stu-id="6adfb-163">Destination field</span></span>
---|---|---
<span data-ttu-id="6adfb-164">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="6adfb-164">LANGUAGEID</span></span> | \> | <span data-ttu-id="6adfb-165">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="6adfb-165">msdyn\_languageid</span></span>
<span data-ttu-id="6adfb-166">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="6adfb-166">NAMEALIAS</span></span> | \> | <span data-ttu-id="6adfb-167">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="6adfb-167">msdyn\_namealias</span></span>
<span data-ttu-id="6adfb-168">NAVN</span><span class="sxs-lookup"><span data-stu-id="6adfb-168">NAME</span></span> | \> | <span data-ttu-id="6adfb-169">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="6adfb-169">msdyn\_name</span></span>
<span data-ttu-id="6adfb-170">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="6adfb-170">PARTYNUMBER</span></span> | \> | <span data-ttu-id="6adfb-171">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="6adfb-171">msdyn\_partynumber</span></span>
<span data-ttu-id="6adfb-172">OPERATINGUNITTYPE</span><span class="sxs-lookup"><span data-stu-id="6adfb-172">OPERATINGUNITTYPE</span></span> | \>\> | <span data-ttu-id="6adfb-173">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="6adfb-173">msdyn\_type</span></span>

### <a name="legal-entity"></a><span data-ttu-id="6adfb-174">Juridisk enhet</span><span class="sxs-lookup"><span data-stu-id="6adfb-174">Legal entity</span></span>

<span data-ttu-id="6adfb-175">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="6adfb-175">Source field</span></span> | <span data-ttu-id="6adfb-176">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="6adfb-176">Map type</span></span> | <span data-ttu-id="6adfb-177">Målfelt</span><span class="sxs-lookup"><span data-stu-id="6adfb-177">Destination field</span></span>
---|---|---
<span data-ttu-id="6adfb-178">NAMEALIAS</span><span class="sxs-lookup"><span data-stu-id="6adfb-178">NAMEALIAS</span></span> | \> | <span data-ttu-id="6adfb-179">msdyn\_namealias</span><span class="sxs-lookup"><span data-stu-id="6adfb-179">msdyn\_namealias</span></span>
<span data-ttu-id="6adfb-180">LANGUAGEID</span><span class="sxs-lookup"><span data-stu-id="6adfb-180">LANGUAGEID</span></span> | \> | <span data-ttu-id="6adfb-181">msdyn\_languageid</span><span class="sxs-lookup"><span data-stu-id="6adfb-181">msdyn\_languageid</span></span>
<span data-ttu-id="6adfb-182">NAVN</span><span class="sxs-lookup"><span data-stu-id="6adfb-182">NAME</span></span> | \> | <span data-ttu-id="6adfb-183">msdyn\_name</span><span class="sxs-lookup"><span data-stu-id="6adfb-183">msdyn\_name</span></span>
<span data-ttu-id="6adfb-184">PARTYNUMBER</span><span class="sxs-lookup"><span data-stu-id="6adfb-184">PARTYNUMBER</span></span> | \> | <span data-ttu-id="6adfb-185">msdyn\_partynumber</span><span class="sxs-lookup"><span data-stu-id="6adfb-185">msdyn\_partynumber</span></span>
<span data-ttu-id="6adfb-186">none</span><span class="sxs-lookup"><span data-stu-id="6adfb-186">none</span></span> | \>\> | <span data-ttu-id="6adfb-187">msdyn\_type</span><span class="sxs-lookup"><span data-stu-id="6adfb-187">msdyn\_type</span></span>
<span data-ttu-id="6adfb-188">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="6adfb-188">LEGALENTITYID</span></span> | \> | <span data-ttu-id="6adfb-189">msdyn\_companycode</span><span class="sxs-lookup"><span data-stu-id="6adfb-189">msdyn\_companycode</span></span>

## <a name="company"></a><span data-ttu-id="6adfb-190">Bedrift</span><span class="sxs-lookup"><span data-stu-id="6adfb-190">Company</span></span>

<span data-ttu-id="6adfb-191">Gir toveissynkronisering av informasjon om juridisk enhet (firma) mellom Finance and Operations og Customer Engagement.</span><span class="sxs-lookup"><span data-stu-id="6adfb-191">Provides bidirectional synchronization of legal entity (company) information between Finance and Operations and Customer Engagement.</span></span>

<!-- ![architecture image](media/dual-write-company.png) -->

<span data-ttu-id="6adfb-192">Kildefelt</span><span class="sxs-lookup"><span data-stu-id="6adfb-192">Source field</span></span> | <span data-ttu-id="6adfb-193">Tilordningstype</span><span class="sxs-lookup"><span data-stu-id="6adfb-193">Map type</span></span> | <span data-ttu-id="6adfb-194">Målfelt</span><span class="sxs-lookup"><span data-stu-id="6adfb-194">Destination field</span></span>
---|---|---
<span data-ttu-id="6adfb-195">NAVN</span><span class="sxs-lookup"><span data-stu-id="6adfb-195">NAME</span></span> | = | <span data-ttu-id="6adfb-196">cdm\_name</span><span class="sxs-lookup"><span data-stu-id="6adfb-196">cdm\_name</span></span>
<span data-ttu-id="6adfb-197">LEGALENTITYID</span><span class="sxs-lookup"><span data-stu-id="6adfb-197">LEGALENTITYID</span></span> | = | <span data-ttu-id="6adfb-198">cdm\_companycode</span><span class="sxs-lookup"><span data-stu-id="6adfb-198">cdm\_companycode</span></span>
