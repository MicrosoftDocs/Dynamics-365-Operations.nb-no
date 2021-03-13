---
title: Vurderingsnivå
description: Dette emnet beskriver Vurderingsnivå-enheten for Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 1ad37c7a5b961bb03d37775168dac91e606d2b08
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125263"
---
# <a name="rating-level"></a><span data-ttu-id="6b014-103">Vurderingsnivå</span><span class="sxs-lookup"><span data-stu-id="6b014-103">Rating level</span></span>

<span data-ttu-id="6b014-104">Dette emnet beskriver Vurderingsnivå-enheten for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6b014-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="6b014-105">Fysisk navn: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="6b014-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="6b014-106">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6b014-106">Description</span></span>

<span data-ttu-id="6b014-107">Denne enheten inneholder tilgjengelige vurderingsnivåer for ferdigheter.</span><span class="sxs-lookup"><span data-stu-id="6b014-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="6b014-108">Vurderingsnivåer gjelder på tvers av alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="6b014-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="6b014-109">JSON-representasjon</span><span class="sxs-lookup"><span data-stu-id="6b014-109">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_factor": Int,
    "mshr_note": "String",
    "mshr_ratinglevelid": "String",
    "mshr_ratingmodelid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_ratingmodelentity_id_value": "Guid",
    "mshr_hcmratinglevelentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="6b014-110">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="6b014-110">Properties</span></span>

| <span data-ttu-id="6b014-111">Egenskap</span><span class="sxs-lookup"><span data-stu-id="6b014-111">Property</span></span><br><span data-ttu-id="6b014-112">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="6b014-112">**Physical name**</span></span><br><span data-ttu-id="6b014-113">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="6b014-113">**_Type_**</span></span> | <span data-ttu-id="6b014-114">Bruk</span><span class="sxs-lookup"><span data-stu-id="6b014-114">Use</span></span> | <span data-ttu-id="6b014-115">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6b014-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6b014-116">**ID for Vurderingsnivå-enhet**</span><span class="sxs-lookup"><span data-stu-id="6b014-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="6b014-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="6b014-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="6b014-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6b014-118">*GUID*</span></span> | <span data-ttu-id="6b014-119">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="6b014-119">Read-only</span></span><br><span data-ttu-id="6b014-120">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="6b014-120">Required</span></span><br><span data-ttu-id="6b014-121">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="6b014-121">System-generated</span></span> | <span data-ttu-id="6b014-122">Den systemgenererte unike identifikatoren for nivået.</span><span class="sxs-lookup"><span data-stu-id="6b014-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="6b014-123">**Vurderingsnivå-ID**</span><span class="sxs-lookup"><span data-stu-id="6b014-123">**Rating Level ID**</span></span><br><span data-ttu-id="6b014-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="6b014-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="6b014-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="6b014-125">*String*</span></span> | <span data-ttu-id="6b014-126">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="6b014-126">Read/write</span></span><br><span data-ttu-id="6b014-127">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="6b014-127">Required</span></span> | <span data-ttu-id="6b014-128">Brukerlesbare unik identifikator for nivået.</span><span class="sxs-lookup"><span data-stu-id="6b014-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="6b014-129">**ID for vurderingsmodell**</span><span class="sxs-lookup"><span data-stu-id="6b014-129">**Rating Model ID**</span></span><br><span data-ttu-id="6b014-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="6b014-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="6b014-131">*Streng*</span><span class="sxs-lookup"><span data-stu-id="6b014-131">*String*</span></span> | <span data-ttu-id="6b014-132">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="6b014-132">Read/write</span></span><br><span data-ttu-id="6b014-133">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="6b014-133">Required</span></span> | <span data-ttu-id="6b014-134">Vurderingsmodellen som vurderingsnivået tilhører.</span><span class="sxs-lookup"><span data-stu-id="6b014-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="6b014-135">**ID for Vurderingsmodell-enhet**</span><span class="sxs-lookup"><span data-stu-id="6b014-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="6b014-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="6b014-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="6b014-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6b014-137">*GUID*</span></span> | <span data-ttu-id="6b014-138">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="6b014-138">Read-only</span></span><br><span data-ttu-id="6b014-139">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="6b014-139">Required</span></span><br><span data-ttu-id="6b014-140">Sekundærnøkkel: mshr_hcmratingmodelentityid i mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="6b014-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="6b014-141">Den systemgenererte IDen for vurderingsmodellen som vurderingsnivået tilhører.</span><span class="sxs-lookup"><span data-stu-id="6b014-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="6b014-142">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="6b014-142">**Description**</span></span><br><span data-ttu-id="6b014-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="6b014-143">mshr_description</span></span><br><span data-ttu-id="6b014-144">*Streng*</span><span class="sxs-lookup"><span data-stu-id="6b014-144">*String*</span></span> | <span data-ttu-id="6b014-145">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="6b014-145">Read/write</span></span><br><span data-ttu-id="6b014-146">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="6b014-146">Required</span></span> | <span data-ttu-id="6b014-147">Beskrivelsen av vurderingsnivået.</span><span class="sxs-lookup"><span data-stu-id="6b014-147">The description of the rating level.</span></span> |
| <span data-ttu-id="6b014-148">**Omregningsfaktor**</span><span class="sxs-lookup"><span data-stu-id="6b014-148">**Factor**</span></span><br><span data-ttu-id="6b014-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="6b014-149">mshr_factor</span></span><br><span data-ttu-id="6b014-150">*Heltall*</span><span class="sxs-lookup"><span data-stu-id="6b014-150">*Integer*</span></span> | <span data-ttu-id="6b014-151">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="6b014-151">Read/write</span></span><br><span data-ttu-id="6b014-152">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="6b014-152">Required</span></span> | <span data-ttu-id="6b014-153">Faktoren for vurderingsnivået.</span><span class="sxs-lookup"><span data-stu-id="6b014-153">The factor for the rating level.</span></span> <span data-ttu-id="6b014-154">Når du sammenligner varer med et annet antall vurderingsnivåer, brukes faktoren til å normalisere poengsummene.</span><span class="sxs-lookup"><span data-stu-id="6b014-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="6b014-155">Verdien må være et heltall mellom 0 og 9.</span><span class="sxs-lookup"><span data-stu-id="6b014-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="6b014-156">**Obs!**</span><span class="sxs-lookup"><span data-stu-id="6b014-156">**Note**</span></span><br><span data-ttu-id="6b014-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="6b014-157">mshr_note</span></span><br><span data-ttu-id="6b014-158">*Streng*</span><span class="sxs-lookup"><span data-stu-id="6b014-158">*String*</span></span> | <span data-ttu-id="6b014-159">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="6b014-159">Read/write</span></span><br><span data-ttu-id="6b014-160">Valgfri</span><span class="sxs-lookup"><span data-stu-id="6b014-160">Optional</span></span> | <span data-ttu-id="6b014-161">Eventuelle merknader som er knyttet til vurderingsnivået.</span><span class="sxs-lookup"><span data-stu-id="6b014-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="6b014-162">**Primærfelt**</span><span class="sxs-lookup"><span data-stu-id="6b014-162">**Primary Field**</span></span><br><span data-ttu-id="6b014-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="6b014-163">mshr_primaryfield</span></span><br><span data-ttu-id="6b014-164">*Streng*</span><span class="sxs-lookup"><span data-stu-id="6b014-164">*String*</span></span> | <span data-ttu-id="6b014-165">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="6b014-165">Read-only</span></span><br><span data-ttu-id="6b014-166">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="6b014-166">Required</span></span> | <span data-ttu-id="6b014-167">Felt som brukes som en identifikator for enhetsposten.</span><span class="sxs-lookup"><span data-stu-id="6b014-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="6b014-168">Kombinasjon av vurderingsnivå-ID og vurderingsmodell-ID.</span><span class="sxs-lookup"><span data-stu-id="6b014-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="6b014-169">Se også</span><span class="sxs-lookup"><span data-stu-id="6b014-169">See also</span></span>

[<span data-ttu-id="6b014-170">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="6b014-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="6b014-171">Eksempelspørring for Kandidat for ansettelse</span><span class="sxs-lookup"><span data-stu-id="6b014-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

