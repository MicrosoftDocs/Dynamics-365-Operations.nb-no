---
title: Vurderingsnivå
description: Dette emnet beskriver Vurderingsnivå-enheten for Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: eac80599de07a045aa233f1cdfd16fe0db8733a2
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5800339"
---
# <a name="rating-level"></a><span data-ttu-id="aa2c6-103">Vurderingsnivå</span><span class="sxs-lookup"><span data-stu-id="aa2c6-103">Rating level</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="aa2c6-104">Dette emnet beskriver Vurderingsnivå-enheten for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="aa2c6-104">This topic describes the Rating level entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="aa2c6-105">Fysisk navn: mshr_hcmratinglevelentity</span><span class="sxs-lookup"><span data-stu-id="aa2c6-105">Physical name: mshr_hcmratinglevelentity</span></span>

## <a name="description"></a><span data-ttu-id="aa2c6-106">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="aa2c6-106">Description</span></span>

<span data-ttu-id="aa2c6-107">Denne enheten inneholder tilgjengelige vurderingsnivåer for ferdigheter.</span><span class="sxs-lookup"><span data-stu-id="aa2c6-107">This entity provides the available rating levels for skills.</span></span> <span data-ttu-id="aa2c6-108">Vurderingsnivåer gjelder på tvers av alle juridiske enheter.</span><span class="sxs-lookup"><span data-stu-id="aa2c6-108">Rating levels apply across all legal entities.</span></span>

## <a name="json-representation"></a><span data-ttu-id="aa2c6-109">JSON-representasjon</span><span class="sxs-lookup"><span data-stu-id="aa2c6-109">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="aa2c6-110">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="aa2c6-110">Properties</span></span>

| <span data-ttu-id="aa2c6-111">Egenskap</span><span class="sxs-lookup"><span data-stu-id="aa2c6-111">Property</span></span><br><span data-ttu-id="aa2c6-112">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="aa2c6-112">**Physical name**</span></span><br><span data-ttu-id="aa2c6-113">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="aa2c6-113">**_Type_**</span></span> | <span data-ttu-id="aa2c6-114">Bruk</span><span class="sxs-lookup"><span data-stu-id="aa2c6-114">Use</span></span> | <span data-ttu-id="aa2c6-115">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="aa2c6-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="aa2c6-116">**ID for Vurderingsnivå-enhet**</span><span class="sxs-lookup"><span data-stu-id="aa2c6-116">**Rating Level Entity ID**</span></span><br><span data-ttu-id="aa2c6-117">mshr_hcmratinglevelentityid</span><span class="sxs-lookup"><span data-stu-id="aa2c6-117">mshr_hcmratinglevelentityid</span></span><br><span data-ttu-id="aa2c6-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="aa2c6-118">*GUID*</span></span> | <span data-ttu-id="aa2c6-119">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="aa2c6-119">Read-only</span></span><br><span data-ttu-id="aa2c6-120">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="aa2c6-120">Required</span></span><br><span data-ttu-id="aa2c6-121">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="aa2c6-121">System-generated</span></span> | <span data-ttu-id="aa2c6-122">Den systemgenererte unike identifikatoren for nivået.</span><span class="sxs-lookup"><span data-stu-id="aa2c6-122">The system-generated unique identifier for the level.</span></span> |
| <span data-ttu-id="aa2c6-123">**Vurderingsnivå-ID**</span><span class="sxs-lookup"><span data-stu-id="aa2c6-123">**Rating Level ID**</span></span><br><span data-ttu-id="aa2c6-124">mshr_ratinglevelid</span><span class="sxs-lookup"><span data-stu-id="aa2c6-124">mshr_ratinglevelid</span></span><br><span data-ttu-id="aa2c6-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="aa2c6-125">*String*</span></span> | <span data-ttu-id="aa2c6-126">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="aa2c6-126">Read/write</span></span><br><span data-ttu-id="aa2c6-127">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="aa2c6-127">Required</span></span> | <span data-ttu-id="aa2c6-128">Brukerlesbare unik identifikator for nivået.</span><span class="sxs-lookup"><span data-stu-id="aa2c6-128">User-readable unique identifier for the level.</span></span> |
| <span data-ttu-id="aa2c6-129">**ID for vurderingsmodell**</span><span class="sxs-lookup"><span data-stu-id="aa2c6-129">**Rating Model ID**</span></span><br><span data-ttu-id="aa2c6-130">mshr_ratingmodelid</span><span class="sxs-lookup"><span data-stu-id="aa2c6-130">mshr_ratingmodelid</span></span><br><span data-ttu-id="aa2c6-131">*Streng*</span><span class="sxs-lookup"><span data-stu-id="aa2c6-131">*String*</span></span> | <span data-ttu-id="aa2c6-132">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="aa2c6-132">Read/write</span></span><br><span data-ttu-id="aa2c6-133">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="aa2c6-133">Required</span></span> | <span data-ttu-id="aa2c6-134">Vurderingsmodellen som vurderingsnivået tilhører.</span><span class="sxs-lookup"><span data-stu-id="aa2c6-134">The rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="aa2c6-135">**ID for Vurderingsmodell-enhet**</span><span class="sxs-lookup"><span data-stu-id="aa2c6-135">**Rating Model Entity ID**</span></span><br><span data-ttu-id="aa2c6-136">_mshr_fk_ratingmodelentity_id_value</span><span class="sxs-lookup"><span data-stu-id="aa2c6-136">_mshr_fk_ratingmodelentity_id_value</span></span><br><span data-ttu-id="aa2c6-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="aa2c6-137">*GUID*</span></span> | <span data-ttu-id="aa2c6-138">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="aa2c6-138">Read-only</span></span><br><span data-ttu-id="aa2c6-139">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="aa2c6-139">Required</span></span><br><span data-ttu-id="aa2c6-140">Sekundærnøkkel: mshr_hcmratingmodelentityid i mshr_hcmratingmodelentity</span><span class="sxs-lookup"><span data-stu-id="aa2c6-140">Foreign key: mshr_hcmratingmodelentityid of mshr_hcmratingmodelentity</span></span> | <span data-ttu-id="aa2c6-141">Den systemgenererte IDen for vurderingsmodellen som vurderingsnivået tilhører.</span><span class="sxs-lookup"><span data-stu-id="aa2c6-141">The system-generated identifier for the rating model to which the rating level belongs.</span></span> |
| <span data-ttu-id="aa2c6-142">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="aa2c6-142">**Description**</span></span><br><span data-ttu-id="aa2c6-143">mshr_description</span><span class="sxs-lookup"><span data-stu-id="aa2c6-143">mshr_description</span></span><br><span data-ttu-id="aa2c6-144">*Streng*</span><span class="sxs-lookup"><span data-stu-id="aa2c6-144">*String*</span></span> | <span data-ttu-id="aa2c6-145">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="aa2c6-145">Read/write</span></span><br><span data-ttu-id="aa2c6-146">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="aa2c6-146">Required</span></span> | <span data-ttu-id="aa2c6-147">Beskrivelsen av vurderingsnivået.</span><span class="sxs-lookup"><span data-stu-id="aa2c6-147">The description of the rating level.</span></span> |
| <span data-ttu-id="aa2c6-148">**Omregningsfaktor**</span><span class="sxs-lookup"><span data-stu-id="aa2c6-148">**Factor**</span></span><br><span data-ttu-id="aa2c6-149">mshr_factor</span><span class="sxs-lookup"><span data-stu-id="aa2c6-149">mshr_factor</span></span><br><span data-ttu-id="aa2c6-150">*Heltall*</span><span class="sxs-lookup"><span data-stu-id="aa2c6-150">*Integer*</span></span> | <span data-ttu-id="aa2c6-151">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="aa2c6-151">Read/write</span></span><br><span data-ttu-id="aa2c6-152">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="aa2c6-152">Required</span></span> | <span data-ttu-id="aa2c6-153">Faktoren for vurderingsnivået.</span><span class="sxs-lookup"><span data-stu-id="aa2c6-153">The factor for the rating level.</span></span> <span data-ttu-id="aa2c6-154">Når du sammenligner varer med et annet antall vurderingsnivåer, brukes faktoren til å normalisere poengsummene.</span><span class="sxs-lookup"><span data-stu-id="aa2c6-154">When you compare items with a different number of rating levels, the factor is used to normalize the scores.</span></span> <span data-ttu-id="aa2c6-155">Verdien må være et heltall mellom 0 og 9.</span><span class="sxs-lookup"><span data-stu-id="aa2c6-155">The value must be an integer between 0 and 9.</span></span> |
| <span data-ttu-id="aa2c6-156">**Obs!**</span><span class="sxs-lookup"><span data-stu-id="aa2c6-156">**Note**</span></span><br><span data-ttu-id="aa2c6-157">mshr_note</span><span class="sxs-lookup"><span data-stu-id="aa2c6-157">mshr_note</span></span><br><span data-ttu-id="aa2c6-158">*Streng*</span><span class="sxs-lookup"><span data-stu-id="aa2c6-158">*String*</span></span> | <span data-ttu-id="aa2c6-159">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="aa2c6-159">Read/write</span></span><br><span data-ttu-id="aa2c6-160">Valgfri</span><span class="sxs-lookup"><span data-stu-id="aa2c6-160">Optional</span></span> | <span data-ttu-id="aa2c6-161">Eventuelle merknader som er knyttet til vurderingsnivået.</span><span class="sxs-lookup"><span data-stu-id="aa2c6-161">Any notes associated with the rating level.</span></span> |
| <span data-ttu-id="aa2c6-162">**Primærfelt**</span><span class="sxs-lookup"><span data-stu-id="aa2c6-162">**Primary Field**</span></span><br><span data-ttu-id="aa2c6-163">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="aa2c6-163">mshr_primaryfield</span></span><br><span data-ttu-id="aa2c6-164">*Streng*</span><span class="sxs-lookup"><span data-stu-id="aa2c6-164">*String*</span></span> | <span data-ttu-id="aa2c6-165">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="aa2c6-165">Read-only</span></span><br><span data-ttu-id="aa2c6-166">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="aa2c6-166">Required</span></span> | <span data-ttu-id="aa2c6-167">Felt som brukes som en identifikator for enhetsposten.</span><span class="sxs-lookup"><span data-stu-id="aa2c6-167">Field to be used as an identifier of the entity record.</span></span> <span data-ttu-id="aa2c6-168">Kombinasjon av vurderingsnivå-ID og vurderingsmodell-ID.</span><span class="sxs-lookup"><span data-stu-id="aa2c6-168">Combination of rating level ID and rating model ID.</span></span> |

## <a name="see-also"></a><span data-ttu-id="aa2c6-169">Se også</span><span class="sxs-lookup"><span data-stu-id="aa2c6-169">See also</span></span>

[<span data-ttu-id="aa2c6-170">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="aa2c6-170">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="aa2c6-171">Eksempelspørring for Kandidat for ansettelse</span><span class="sxs-lookup"><span data-stu-id="aa2c6-171">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]