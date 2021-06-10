---
title: Personscreening
description: Dette emnet beskriver Personscreening-enheten for Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 9d29b26094e307c3f68d57f297ab3614f3a5ccae
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059286"
---
# <a name="person-screening"></a><span data-ttu-id="b53b5-103">Personscreening</span><span class="sxs-lookup"><span data-stu-id="b53b5-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b53b5-104">Dette emnet beskriver Personscreening-enheten for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b53b5-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="b53b5-105">Fysisk navn: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="b53b5-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="b53b5-106">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b53b5-106">Description</span></span>

<span data-ttu-id="b53b5-107">Denne enheten beskriver screeninger en kandidat har bestått eller må bestå for ansettelse.</span><span class="sxs-lookup"><span data-stu-id="b53b5-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b53b5-108">JSON-representasjon</span><span class="sxs-lookup"><span data-stu-id="b53b5-108">JSON representation</span></span>

```json
{
    "mshr_note": "String",
    "mshr_requiredby": "Date",
    "mshr_status": Int,
    "mshr_partynumber": "String",
    "mshr_screeningtypeid": "String",
    "mshr_primaryfield": "String",
    "_mshr_fk_person_id_value": "Guid",
    "mshr_hcmpersonscreeningentityid": "Guid",
    "mshr_completeddate": "Date"
}
```

## <a name="properties"></a><span data-ttu-id="b53b5-109">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="b53b5-109">Properties</span></span>

| <span data-ttu-id="b53b5-110">Egenskap</span><span class="sxs-lookup"><span data-stu-id="b53b5-110">Property</span></span><br><span data-ttu-id="b53b5-111">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="b53b5-111">**Physical name**</span></span><br><span data-ttu-id="b53b5-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="b53b5-112">**_Type_**</span></span> | <span data-ttu-id="b53b5-113">Bruk</span><span class="sxs-lookup"><span data-stu-id="b53b5-113">Use</span></span> | <span data-ttu-id="b53b5-114">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b53b5-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b53b5-115">**Enhets-ID for personens screening**</span><span class="sxs-lookup"><span data-stu-id="b53b5-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="b53b5-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="b53b5-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="b53b5-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b53b5-117">*GUID*</span></span> | <span data-ttu-id="b53b5-118">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="b53b5-118">Read-only</span></span><br><span data-ttu-id="b53b5-119">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b53b5-119">Required</span></span><br><span data-ttu-id="b53b5-120">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="b53b5-120">System-generated</span></span> | <span data-ttu-id="b53b5-121">Unik primær-ID for posten for personscreening.</span><span class="sxs-lookup"><span data-stu-id="b53b5-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="b53b5-122">**Partsnummer**</span><span class="sxs-lookup"><span data-stu-id="b53b5-122">**Party Number**</span></span><br><span data-ttu-id="b53b5-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="b53b5-123">mshr_partynumber</span></span><br><span data-ttu-id="b53b5-124">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b53b5-124">*String*</span></span> | <span data-ttu-id="b53b5-125">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="b53b5-125">Read/write</span></span><br><span data-ttu-id="b53b5-126">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b53b5-126">Required</span></span> | <span data-ttu-id="b53b5-127">Partnummeret (person) tilknyttet kandidaten.</span><span class="sxs-lookup"><span data-stu-id="b53b5-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="b53b5-128">**Verdi for person-ID**</span><span class="sxs-lookup"><span data-stu-id="b53b5-128">**Person ID Value**</span></span><br><span data-ttu-id="b53b5-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="b53b5-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="b53b5-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b53b5-130">*GUID*</span></span> | <span data-ttu-id="b53b5-131">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="b53b5-131">Read-only</span></span><br><span data-ttu-id="b53b5-132">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b53b5-132">Required</span></span><br><span data-ttu-id="b53b5-133">Sekundærnøkkel: mshr_dirpersonentityid i mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="b53b5-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="b53b5-134">Systemgenerert unik identifikator for partsenhetsposten (person).</span><span class="sxs-lookup"><span data-stu-id="b53b5-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="b53b5-135">**ID for screeningtype**</span><span class="sxs-lookup"><span data-stu-id="b53b5-135">**Screening Type ID**</span></span><br><span data-ttu-id="b53b5-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="b53b5-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="b53b5-137">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b53b5-137">*String*</span></span> | <span data-ttu-id="b53b5-138">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="b53b5-138">Read/write</span></span><br><span data-ttu-id="b53b5-139">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b53b5-139">Required</span></span><br><span data-ttu-id="b53b5-140">Sekundærnøkkel: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="b53b5-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="b53b5-141">IDen for screeningtype som er definert i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b53b5-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="b53b5-142">**Verdi for ID for screeningtype**</span><span class="sxs-lookup"><span data-stu-id="b53b5-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="b53b5-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="b53b5-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="b53b5-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b53b5-144">*GUID*</span></span> | <span data-ttu-id="b53b5-145">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="b53b5-145">Read-only</span></span><br><span data-ttu-id="b53b5-146">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b53b5-146">Required</span></span><br><span data-ttu-id="b53b5-147">Sekundærnøkkel: mshr_hcmscreeningtypeentityid i mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="b53b5-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="b53b5-148">Systemgenerert identifikator for skjermtypeposten i den tilknyttede enheten.</span><span class="sxs-lookup"><span data-stu-id="b53b5-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="b53b5-149">**Kreves innen**</span><span class="sxs-lookup"><span data-stu-id="b53b5-149">**Required By**</span></span><br><span data-ttu-id="b53b5-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="b53b5-150">mshr_requiredby</span></span><br><span data-ttu-id="b53b5-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="b53b5-151">*Datetime*</span></span> | <span data-ttu-id="b53b5-152">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="b53b5-152">Read/write</span></span><br><span data-ttu-id="b53b5-153">Valgfri</span><span class="sxs-lookup"><span data-stu-id="b53b5-153">Optional</span></span> | <span data-ttu-id="b53b5-154">Datoen som skjermbildet må fullføres innen.</span><span class="sxs-lookup"><span data-stu-id="b53b5-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="b53b5-155">**Status**</span><span class="sxs-lookup"><span data-stu-id="b53b5-155">**Status**</span></span><br><span data-ttu-id="b53b5-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="b53b5-156">mshr_status</span></span><br><span data-ttu-id="b53b5-157">*mshr_hcmcompletionstatus-alternativsett*</span><span class="sxs-lookup"><span data-stu-id="b53b5-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="b53b5-158">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="b53b5-158">Read/write</span></span><br><span data-ttu-id="b53b5-159">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b53b5-159">Required</span></span> | <span data-ttu-id="b53b5-160">Gir kandidatens status for screeningen.</span><span class="sxs-lookup"><span data-stu-id="b53b5-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="b53b5-161">**Fullføringsdato**</span><span class="sxs-lookup"><span data-stu-id="b53b5-161">**Completed Date**</span></span><br><span data-ttu-id="b53b5-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="b53b5-162">mshr_completeddate</span></span><br><span data-ttu-id="b53b5-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="b53b5-163">*Datetime*</span></span> | <span data-ttu-id="b53b5-164">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="b53b5-164">Read/write</span></span><br><span data-ttu-id="b53b5-165">Valgfri</span><span class="sxs-lookup"><span data-stu-id="b53b5-165">Optional</span></span> | <span data-ttu-id="b53b5-166">Datoen da screeningen ble fullført.</span><span class="sxs-lookup"><span data-stu-id="b53b5-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="b53b5-167">**Notater**</span><span class="sxs-lookup"><span data-stu-id="b53b5-167">**Notes**</span></span><br><span data-ttu-id="b53b5-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="b53b5-168">mshr_note</span></span><br><span data-ttu-id="b53b5-169">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b53b5-169">*String*</span></span> | <span data-ttu-id="b53b5-170">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="b53b5-170">Read/write</span></span><br><span data-ttu-id="b53b5-171">Valgfri</span><span class="sxs-lookup"><span data-stu-id="b53b5-171">Optional</span></span> | <span data-ttu-id="b53b5-172">Merknader som skal brukes av ansettelsesansvarlige og rekrutteringspersoner.</span><span class="sxs-lookup"><span data-stu-id="b53b5-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="b53b5-173">Se også</span><span class="sxs-lookup"><span data-stu-id="b53b5-173">See also</span></span>

[<span data-ttu-id="b53b5-174">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="b53b5-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="b53b5-175">Eksempelspørring for Kandidat for ansettelse</span><span class="sxs-lookup"><span data-stu-id="b53b5-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]