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
ms.openlocfilehash: 2dbdbea7087d8bca8563da10d1bf9a97df24e8b3
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464748"
---
# <a name="rating-level"></a><span data-ttu-id="fd80d-103">Vurderingsnivå</span><span class="sxs-lookup"><span data-stu-id="fd80d-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="fd80d-104">Dette emnet beskriver Vurderingsnivå-enheten for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="fd80d-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="fd80d-105">Fysisk navn: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="fd80d-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="fd80d-106">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fd80d-106">Description</span></span>

<span data-ttu-id="fd80d-107">Denne enheten inneholder tilgjengelige vurderingsnivåer for ferdigheter.</span><span class="sxs-lookup"><span data-stu-id="fd80d-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="fd80d-108">Vurderingsnivåer gjelder på tvers av alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="fd80d-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="fd80d-109">JSON-representasjon</span><span class="sxs-lookup"><span data-stu-id="fd80d-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="fd80d-110">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="fd80d-110">Properties</span></span>

| <span data-ttu-id="fd80d-111">Egenskap</span><span class="sxs-lookup"><span data-stu-id="fd80d-111">Property</span></span><br><span data-ttu-id="fd80d-112">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="fd80d-112">**Physical name**</span></span><br><span data-ttu-id="fd80d-113">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="fd80d-113">**_Type_**</span></span> | <span data-ttu-id="fd80d-114">Bruk</span><span class="sxs-lookup"><span data-stu-id="fd80d-114">Use</span></span> | <span data-ttu-id="fd80d-115">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fd80d-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fd80d-116">**ID for Vurderingsnivå-enhet**</span><span class="sxs-lookup"><span data-stu-id="fd80d-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="fd80d-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="fd80d-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="fd80d-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="fd80d-118">*GUID*</span></span> | <span data-ttu-id="fd80d-119">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="fd80d-119">Read-only</span></span><br><span data-ttu-id="fd80d-120">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="fd80d-120">Required</span></span><br><span data-ttu-id="fd80d-121">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="fd80d-121">System-generated</span></span> | <span data-ttu-id="fd80d-122">Den systemgenererte unike identifikatoren for nivået.</span><span class="sxs-lookup"><span data-stu-id="fd80d-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="fd80d-123">**Vurderingsnivå-ID**</span><span class="sxs-lookup"><span data-stu-id="fd80d-123">**Rating Level ID**</span></span><br><span data-ttu-id="fd80d-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="fd80d-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="fd80d-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="fd80d-125">*String*</span></span> | <span data-ttu-id="fd80d-126">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="fd80d-126">Read/write</span></span><br><span data-ttu-id="fd80d-127">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="fd80d-127">Required</span></span> | <span data-ttu-id="fd80d-128">Brukerlesbare unik identifikator for nivået.</span><span class="sxs-lookup"><span data-stu-id="fd80d-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="fd80d-129">**ID for vurderingsmodell**</span><span class="sxs-lookup"><span data-stu-id="fd80d-129">**Rating Model ID**</span></span><br><span data-ttu-id="fd80d-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="fd80d-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="fd80d-131">*Streng*</span><span class="sxs-lookup"><span data-stu-id="fd80d-131">*String*</span></span> | <span data-ttu-id="fd80d-132">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="fd80d-132">Read/write</span></span><br><span data-ttu-id="fd80d-133">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="fd80d-133">Required</span></span> | <span data-ttu-id="fd80d-134">Vurderingsmodellen som vurderingsnivået tilhører.</span><span class="sxs-lookup"><span data-stu-id="fd80d-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="fd80d-135">**ID for Vurderingsmodell-enhet**</span><span class="sxs-lookup"><span data-stu-id="fd80d-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="fd80d-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="fd80d-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="fd80d-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="fd80d-137">*GUID*</span></span> | <span data-ttu-id="fd80d-138">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="fd80d-138">Read-only</span></span><br><span data-ttu-id="fd80d-139">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="fd80d-139">Required</span></span><br><span data-ttu-id="fd80d-140">Sekundærnøkkel: mshr_hcmratingmodelentityid i mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="fd80d-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="fd80d-141">Den systemgenererte IDen for vurderingsmodellen som vurderingsnivået tilhører.</span><span class="sxs-lookup"><span data-stu-id="fd80d-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="fd80d-142">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="fd80d-142">**Description**</span></span><br><span data-ttu-id="fd80d-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="fd80d-143">mshr_description</span></span><br><span data-ttu-id="fd80d-144">*Streng*</span><span class="sxs-lookup"><span data-stu-id="fd80d-144">*String*</span></span> | <span data-ttu-id="fd80d-145">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="fd80d-145">Read/write</span></span><br><span data-ttu-id="fd80d-146">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="fd80d-146">Required</span></span> | <span data-ttu-id="fd80d-147">Beskrivelsen av vurderingsnivået.</span><span class="sxs-lookup"><span data-stu-id="fd80d-147">The description of the rating level.</span></span> |
| <span data-ttu-id="fd80d-148">**Omregningsfaktor**</span><span class="sxs-lookup"><span data-stu-id="fd80d-148">**Factor**</span></span><br><span data-ttu-id="fd80d-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="fd80d-149">mshr_factor</span></span><br><span data-ttu-id="fd80d-150">*Heltall*</span><span class="sxs-lookup"><span data-stu-id="fd80d-150">*Integer*</span></span> | <span data-ttu-id="fd80d-151">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="fd80d-151">Read/write</span></span><br><span data-ttu-id="fd80d-152">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="fd80d-152">Required</span></span> | <span data-ttu-id="fd80d-153">Faktoren for vurderingsnivået.</span><span class="sxs-lookup"><span data-stu-id="fd80d-153">The factor for the rating level.</span></span> <span data-ttu-id="fd80d-154">Når du sammenligner varer med et annet antall vurderingsnivåer, brukes faktoren til å normalisere poengsummene.</span><span class="sxs-lookup"><span data-stu-id="fd80d-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="fd80d-155">Verdien må være et heltall mellom 0 og 9.</span><span class="sxs-lookup"><span data-stu-id="fd80d-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="fd80d-156">**Obs!**</span><span class="sxs-lookup"><span data-stu-id="fd80d-156">**Note**</span></span><br><span data-ttu-id="fd80d-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="fd80d-157">mshr_note</span></span><br><span data-ttu-id="fd80d-158">*Streng*</span><span class="sxs-lookup"><span data-stu-id="fd80d-158">*String*</span></span> | <span data-ttu-id="fd80d-159">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="fd80d-159">Read/write</span></span><br><span data-ttu-id="fd80d-160">Valgfri</span><span class="sxs-lookup"><span data-stu-id="fd80d-160">Optional</span></span> | <span data-ttu-id="fd80d-161">Eventuelle merknader som er knyttet til vurderingsnivået.</span><span class="sxs-lookup"><span data-stu-id="fd80d-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="fd80d-162">**Primærfelt**</span><span class="sxs-lookup"><span data-stu-id="fd80d-162">**Primary Field**</span></span><br><span data-ttu-id="fd80d-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="fd80d-163">mshr_primaryfield</span></span><br><span data-ttu-id="fd80d-164">*Streng*</span><span class="sxs-lookup"><span data-stu-id="fd80d-164">*String*</span></span> | <span data-ttu-id="fd80d-165">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="fd80d-165">Read-only</span></span><br><span data-ttu-id="fd80d-166">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="fd80d-166">Required</span></span> | <span data-ttu-id="fd80d-167">Felt som brukes som en identifikator for enhetsposten.</span><span class="sxs-lookup"><span data-stu-id="fd80d-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="fd80d-168">Kombinasjon av vurderingsnivå-ID og vurderingsmodell-ID.</span><span class="sxs-lookup"><span data-stu-id="fd80d-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="fd80d-169">Se også</span><span class="sxs-lookup"><span data-stu-id="fd80d-169">See also</span></span>

[<span data-ttu-id="fd80d-170">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="fd80d-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="fd80d-171">Eksempelspørring for Kandidat for ansettelse</span><span class="sxs-lookup"><span data-stu-id="fd80d-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]