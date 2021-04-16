---
title: Personscreening
description: Dette emnet beskriver Personscreening-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 4bc32eb948f4a4966a927b0907b8d499486e43dc
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798039"
---
# <a name="person-screening"></a><span data-ttu-id="b57e7-103">Personscreening</span><span class="sxs-lookup"><span data-stu-id="b57e7-103">Person screening</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="b57e7-104">Dette emnet beskriver Personscreening-enheten for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b57e7-104">This topic describes the Person screening entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="b57e7-105">Fysisk navn: mshr_hcmpersonscreeningentity</span><span class="sxs-lookup"><span data-stu-id="b57e7-105">Physical name: mshr_hcmpersonscreeningentity</span></span>

## <a name="description"></a><span data-ttu-id="b57e7-106">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b57e7-106">Description</span></span>

<span data-ttu-id="b57e7-107">Denne enheten beskriver screeninger en kandidat har bestått eller må bestå for ansettelse.</span><span class="sxs-lookup"><span data-stu-id="b57e7-107">This entity describes screenings a candidate has passed or must pass for employment.</span></span>

## <a name="json-representation"></a><span data-ttu-id="b57e7-108">JSON-representasjon</span><span class="sxs-lookup"><span data-stu-id="b57e7-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="b57e7-109">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="b57e7-109">Properties</span></span>

| <span data-ttu-id="b57e7-110">Egenskap</span><span class="sxs-lookup"><span data-stu-id="b57e7-110">Property</span></span><br><span data-ttu-id="b57e7-111">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="b57e7-111">**Physical name**</span></span><br><span data-ttu-id="b57e7-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="b57e7-112">**_Type_**</span></span> | <span data-ttu-id="b57e7-113">Bruk</span><span class="sxs-lookup"><span data-stu-id="b57e7-113">Use</span></span> | <span data-ttu-id="b57e7-114">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="b57e7-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="b57e7-115">**Enhets-ID for personens screening**</span><span class="sxs-lookup"><span data-stu-id="b57e7-115">**Person Screening Entity ID**</span></span><br><span data-ttu-id="b57e7-116">mshr_hcmpersonscreeningentityid</span><span class="sxs-lookup"><span data-stu-id="b57e7-116">mshr_hcmpersonscreeningentityid</span></span><br><span data-ttu-id="b57e7-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b57e7-117">*GUID*</span></span> | <span data-ttu-id="b57e7-118">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="b57e7-118">Read-only</span></span><br><span data-ttu-id="b57e7-119">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b57e7-119">Required</span></span><br><span data-ttu-id="b57e7-120">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="b57e7-120">System-generated</span></span> | <span data-ttu-id="b57e7-121">Unik primær-ID for posten for personscreening.</span><span class="sxs-lookup"><span data-stu-id="b57e7-121">Unique primary identifier for the person screening record.</span></span> |
| <span data-ttu-id="b57e7-122">**Partsnummer**</span><span class="sxs-lookup"><span data-stu-id="b57e7-122">**Party Number**</span></span><br><span data-ttu-id="b57e7-123">mshr_partynumber</span><span class="sxs-lookup"><span data-stu-id="b57e7-123">mshr_partynumber</span></span><br><span data-ttu-id="b57e7-124">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b57e7-124">*String*</span></span> | <span data-ttu-id="b57e7-125">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="b57e7-125">Read/write</span></span><br><span data-ttu-id="b57e7-126">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b57e7-126">Required</span></span> | <span data-ttu-id="b57e7-127">Partnummeret (person) tilknyttet kandidaten.</span><span class="sxs-lookup"><span data-stu-id="b57e7-127">The party (person) number associated with the candidate.</span></span> |
| <span data-ttu-id="b57e7-128">**Verdi for person-ID**</span><span class="sxs-lookup"><span data-stu-id="b57e7-128">**Person ID Value**</span></span><br><span data-ttu-id="b57e7-129">_mshr_fk_person_id_value</span><span class="sxs-lookup"><span data-stu-id="b57e7-129">_mshr_fk_person_id_value</span></span><br><span data-ttu-id="b57e7-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b57e7-130">*GUID*</span></span> | <span data-ttu-id="b57e7-131">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="b57e7-131">Read-only</span></span><br><span data-ttu-id="b57e7-132">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b57e7-132">Required</span></span><br><span data-ttu-id="b57e7-133">Sekundærnøkkel: mshr_dirpersonentityid i mshr_dirpersonentity</span><span class="sxs-lookup"><span data-stu-id="b57e7-133">Foreign key: mshr_dirpersonentityid of mshr_dirpersonentity</span></span> | <span data-ttu-id="b57e7-134">Systemgenerert unik identifikator for partsenhetsposten (person).</span><span class="sxs-lookup"><span data-stu-id="b57e7-134">The system-generated identifier of the party (person) entity record.</span></span> |
| <span data-ttu-id="b57e7-135">**ID for screeningtype**</span><span class="sxs-lookup"><span data-stu-id="b57e7-135">**Screening Type ID**</span></span><br><span data-ttu-id="b57e7-136">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="b57e7-136">mshr_screeningtypeid</span></span><br><span data-ttu-id="b57e7-137">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b57e7-137">*String*</span></span> | <span data-ttu-id="b57e7-138">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="b57e7-138">Read/write</span></span><br><span data-ttu-id="b57e7-139">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b57e7-139">Required</span></span><br><span data-ttu-id="b57e7-140">Sekundærnøkkel: ScreeningType</span><span class="sxs-lookup"><span data-stu-id="b57e7-140">Foreign key: ScreeningType</span></span> | <span data-ttu-id="b57e7-141">IDen for screeningtype som er definert i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="b57e7-141">The identifier of the screening type defined in Human Resources.</span></span> |
| <span data-ttu-id="b57e7-142">**Verdi for ID for screeningtype**</span><span class="sxs-lookup"><span data-stu-id="b57e7-142">**Screening Type ID Value**</span></span><br><span data-ttu-id="b57e7-143">_mshr_fk_screeningtype_id_value</span><span class="sxs-lookup"><span data-stu-id="b57e7-143">_mshr_fk_screeningtype_id_value</span></span><br><span data-ttu-id="b57e7-144">*GUID*</span><span class="sxs-lookup"><span data-stu-id="b57e7-144">*GUID*</span></span> | <span data-ttu-id="b57e7-145">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="b57e7-145">Read-only</span></span><br><span data-ttu-id="b57e7-146">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b57e7-146">Required</span></span><br><span data-ttu-id="b57e7-147">Sekundærnøkkel: mshr_hcmscreeningtypeentityid i mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="b57e7-147">Foreign key: mshr_hcmscreeningtypeentityid of mshr_hcmscreeningtypeentity</span></span> | <span data-ttu-id="b57e7-148">Systemgenerert identifikator for skjermtypeposten i den tilknyttede enheten.</span><span class="sxs-lookup"><span data-stu-id="b57e7-148">System-generated identifier for the screening type record in the associated entity.</span></span> |
| <span data-ttu-id="b57e7-149">**Kreves innen**</span><span class="sxs-lookup"><span data-stu-id="b57e7-149">**Required By**</span></span><br><span data-ttu-id="b57e7-150">mshr_requiredby</span><span class="sxs-lookup"><span data-stu-id="b57e7-150">mshr_requiredby</span></span><br><span data-ttu-id="b57e7-151">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="b57e7-151">*Datetime*</span></span> | <span data-ttu-id="b57e7-152">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="b57e7-152">Read/write</span></span><br><span data-ttu-id="b57e7-153">Valgfri</span><span class="sxs-lookup"><span data-stu-id="b57e7-153">Optional</span></span> | <span data-ttu-id="b57e7-154">Datoen som skjermbildet må fullføres innen.</span><span class="sxs-lookup"><span data-stu-id="b57e7-154">The date by which the screening is required to be completed.</span></span> |
| <span data-ttu-id="b57e7-155">**Status**</span><span class="sxs-lookup"><span data-stu-id="b57e7-155">**Status**</span></span><br><span data-ttu-id="b57e7-156">mshr_status</span><span class="sxs-lookup"><span data-stu-id="b57e7-156">mshr_status</span></span><br><span data-ttu-id="b57e7-157">*mshr_hcmcompletionstatus-alternativsett*</span><span class="sxs-lookup"><span data-stu-id="b57e7-157">*mshr_hcmcompletionstatus option set*</span></span><br><span data-ttu-id="b57e7-158">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="b57e7-158">Read/write</span></span><br><span data-ttu-id="b57e7-159">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="b57e7-159">Required</span></span> | <span data-ttu-id="b57e7-160">Gir kandidatens status for screeningen.</span><span class="sxs-lookup"><span data-stu-id="b57e7-160">Provides the candidate’s status for the screening.</span></span> |
| <span data-ttu-id="b57e7-161">**Fullføringsdato**</span><span class="sxs-lookup"><span data-stu-id="b57e7-161">**Completed Date**</span></span><br><span data-ttu-id="b57e7-162">mshr_completeddate</span><span class="sxs-lookup"><span data-stu-id="b57e7-162">mshr_completeddate</span></span><br><span data-ttu-id="b57e7-163">*Datetime*</span><span class="sxs-lookup"><span data-stu-id="b57e7-163">*Datetime*</span></span> | <span data-ttu-id="b57e7-164">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="b57e7-164">Read/write</span></span><br><span data-ttu-id="b57e7-165">Valgfri</span><span class="sxs-lookup"><span data-stu-id="b57e7-165">Optional</span></span> | <span data-ttu-id="b57e7-166">Datoen da screeningen ble fullført.</span><span class="sxs-lookup"><span data-stu-id="b57e7-166">The date the screening was completed.</span></span> |
| <span data-ttu-id="b57e7-167">**Notater**</span><span class="sxs-lookup"><span data-stu-id="b57e7-167">**Notes**</span></span><br><span data-ttu-id="b57e7-168">mshr_note</span><span class="sxs-lookup"><span data-stu-id="b57e7-168">mshr_note</span></span><br><span data-ttu-id="b57e7-169">*Streng*</span><span class="sxs-lookup"><span data-stu-id="b57e7-169">*String*</span></span> | <span data-ttu-id="b57e7-170">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="b57e7-170">Read/write</span></span><br><span data-ttu-id="b57e7-171">Valgfri</span><span class="sxs-lookup"><span data-stu-id="b57e7-171">Optional</span></span> | <span data-ttu-id="b57e7-172">Merknader som skal brukes av ansettelsesansvarlige og rekrutteringspersoner.</span><span class="sxs-lookup"><span data-stu-id="b57e7-172">Notes for use by hiring managers and recruiters.</span></span> |

## <a name="see-also"></a><span data-ttu-id="b57e7-173">Se også</span><span class="sxs-lookup"><span data-stu-id="b57e7-173">See also</span></span>

[<span data-ttu-id="b57e7-174">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="b57e7-174">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="b57e7-175">Eksempelspørring for Kandidat for ansettelse</span><span class="sxs-lookup"><span data-stu-id="b57e7-175">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]