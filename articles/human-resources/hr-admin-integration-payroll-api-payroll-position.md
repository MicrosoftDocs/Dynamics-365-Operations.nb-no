---
title: Lønnsdetaljer for stillinger
description: Dette emnet inneholder informasjon og en eksempelspørring for lønnsdetaljene for Stillinger-enheten i Dynamics 365 Human Resources.
author: jcart
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 8918044dbf84e79015dc3bca904f204123a37db8
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6056786"
---
# <a name="payroll-position"></a><span data-ttu-id="99c21-103">Lønnsstilling</span><span class="sxs-lookup"><span data-stu-id="99c21-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="99c21-104">Dette emnet inneholder informasjon og en eksempelspørring for lønnsdetaljene for Stillinger-enheten i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="99c21-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="99c21-105">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="99c21-105">Properties</span></span>

| <span data-ttu-id="99c21-106">Egenskap</span><span class="sxs-lookup"><span data-stu-id="99c21-106">Property</span></span><br><span data-ttu-id="99c21-107">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="99c21-107">**Physical name**</span></span><br><span data-ttu-id="99c21-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="99c21-108">**_Type_**</span></span> | <span data-ttu-id="99c21-109">Bruk</span><span class="sxs-lookup"><span data-stu-id="99c21-109">Use</span></span> | <span data-ttu-id="99c21-110">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="99c21-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="99c21-111">**Årlige vanlige timer**</span><span class="sxs-lookup"><span data-stu-id="99c21-111">**Annual regular hours**</span></span><br><span data-ttu-id="99c21-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="99c21-112">annualregularhours</span></span><br><span data-ttu-id="99c21-113">*Desimal*</span><span class="sxs-lookup"><span data-stu-id="99c21-113">*Decimal*</span></span> | <span data-ttu-id="99c21-114">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="99c21-114">Read-only</span></span><br><span data-ttu-id="99c21-115">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="99c21-115">Required</span></span> | <span data-ttu-id="99c21-116">Årlige faste timer definert i stillingen.</span><span class="sxs-lookup"><span data-stu-id="99c21-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="99c21-117">**Enhets-ID for lønnsstillingsdetaljer**</span><span class="sxs-lookup"><span data-stu-id="99c21-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="99c21-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="99c21-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="99c21-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="99c21-119">*Guid*</span></span> | <span data-ttu-id="99c21-120">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="99c21-120">Required</span></span><br><span data-ttu-id="99c21-121">Systemgenerert.</span><span class="sxs-lookup"><span data-stu-id="99c21-121">System generated.</span></span> | <span data-ttu-id="99c21-122">En systemgenerert GUID-verdi som entydig identifiserer stillingen.</span><span class="sxs-lookup"><span data-stu-id="99c21-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="99c21-123">**Primærfelt**</span><span class="sxs-lookup"><span data-stu-id="99c21-123">**Primary field**</span></span><br><span data-ttu-id="99c21-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="99c21-124">mshr_primaryfield</span></span><br><span data-ttu-id="99c21-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="99c21-125">*String*</span></span> | <span data-ttu-id="99c21-126">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="99c21-126">Required</span></span><br><span data-ttu-id="99c21-127">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="99c21-127">System generated</span></span> |  |
| <span data-ttu-id="99c21-128">**ID-verdi for stillingsjobb**</span><span class="sxs-lookup"><span data-stu-id="99c21-128">**Position job ID value**</span></span><br><span data-ttu-id="99c21-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="99c21-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="99c21-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="99c21-130">*GUID*</span></span> | <span data-ttu-id="99c21-131">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="99c21-131">Read-only</span></span><br><span data-ttu-id="99c21-132">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="99c21-132">Required</span></span><br><span data-ttu-id="99c21-133">Sekundærnøkkel: mshr_PayrollPositionJobEntity av mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="99c21-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="99c21-134">ID-en for jobben som er knyttet til stillingen.</span><span class="sxs-lookup"><span data-stu-id="99c21-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="99c21-135">**ID-verdi for fast kompensasjonsplan**</span><span class="sxs-lookup"><span data-stu-id="99c21-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="99c21-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="99c21-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="99c21-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="99c21-137">*GUID*</span></span> | <span data-ttu-id="99c21-138">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="99c21-138">Read-only</span></span><br><span data-ttu-id="99c21-139">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="99c21-139">Required</span></span><br><span data-ttu-id="99c21-140">Sekundærnøkkel: mshr_FixedCompPlan_id av mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="99c21-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="99c21-141">ID-en for den faste kompensasjonsplanen som er knyttet til stillingen.</span><span class="sxs-lookup"><span data-stu-id="99c21-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="99c21-142">**ID for lønnssyklus**</span><span class="sxs-lookup"><span data-stu-id="99c21-142">**Pay cycle ID**</span></span><br><span data-ttu-id="99c21-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="99c21-143">mshr_primaryfield</span></span><br><span data-ttu-id="99c21-144">*Streng*</span><span class="sxs-lookup"><span data-stu-id="99c21-144">*String*</span></span> | <span data-ttu-id="99c21-145">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="99c21-145">Read-only</span></span><br><span data-ttu-id="99c21-146">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="99c21-146">Required</span></span> | <span data-ttu-id="99c21-147">Lønnssyklusen som er definert for stillingen.</span><span class="sxs-lookup"><span data-stu-id="99c21-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="99c21-148">**Betalt av juridisk enhet**</span><span class="sxs-lookup"><span data-stu-id="99c21-148">**Paid by legal entity**</span></span><br><span data-ttu-id="99c21-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="99c21-149">paidbylegalentity</span></span><br><span data-ttu-id="99c21-150">*Streng*</span><span class="sxs-lookup"><span data-stu-id="99c21-150">*String*</span></span> | <span data-ttu-id="99c21-151">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="99c21-151">Read-only</span></span><br><span data-ttu-id="99c21-152">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="99c21-152">Required</span></span> | <span data-ttu-id="99c21-153">Den juridiske enheten som er definert i stillingen som er ansvarlig for utstedelse av betaling.</span><span class="sxs-lookup"><span data-stu-id="99c21-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="99c21-154">**Stillings-ID**</span><span class="sxs-lookup"><span data-stu-id="99c21-154">**Position ID**</span></span><br><span data-ttu-id="99c21-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="99c21-155">mshr_positionid</span></span><br><span data-ttu-id="99c21-156">*Streng*</span><span class="sxs-lookup"><span data-stu-id="99c21-156">*String*</span></span> | <span data-ttu-id="99c21-157">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="99c21-157">Read-only</span></span><br><span data-ttu-id="99c21-158">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="99c21-158">Required</span></span> | <span data-ttu-id="99c21-159">ID-en for stillingen.</span><span class="sxs-lookup"><span data-stu-id="99c21-159">The ID of the position.</span></span> |
| <span data-ttu-id="99c21-160">**Gyldig til**</span><span class="sxs-lookup"><span data-stu-id="99c21-160">**Valid to**</span></span><br><span data-ttu-id="99c21-161">validto</span><span class="sxs-lookup"><span data-stu-id="99c21-161">validto</span></span><br><span data-ttu-id="99c21-162">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="99c21-162">*Date Time Offset*</span></span> | <span data-ttu-id="99c21-163">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="99c21-163">Read-only</span></span><br><span data-ttu-id="99c21-164">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="99c21-164">Required</span></span> |<span data-ttu-id="99c21-165">Datoen stillingsdetaljene er gyldige fra.</span><span class="sxs-lookup"><span data-stu-id="99c21-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="99c21-166">**Gyldig fra**</span><span class="sxs-lookup"><span data-stu-id="99c21-166">**Valid from**</span></span><br><span data-ttu-id="99c21-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="99c21-167">validfrom</span></span><br><span data-ttu-id="99c21-168">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="99c21-168">*Date Time Offset*</span></span> | <span data-ttu-id="99c21-169">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="99c21-169">Read-only</span></span><br><span data-ttu-id="99c21-170">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="99c21-170">Required</span></span> |<span data-ttu-id="99c21-171">Datoen stillingsdetaljene er gyldige til.</span><span class="sxs-lookup"><span data-stu-id="99c21-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="99c21-172">**Forespørsel**</span><span class="sxs-lookup"><span data-stu-id="99c21-172">**Query**</span></span>

<span data-ttu-id="99c21-173">**Forespørsel**</span><span class="sxs-lookup"><span data-stu-id="99c21-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="99c21-174">**Svar**</span><span class="sxs-lookup"><span data-stu-id="99c21-174">**Response**</span></span>

```json
{
            "mshr_positionid": "000276",
            "mshr_paycycleid": "w",
            "mshr_annualregularhours": 3000,
            "mshr_paidbylegalentity": "USMF",
            "mshr_validfrom": "2021-03-14T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_primaryfield": "000276 | 3/14/2021",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollpositionentityid": "00010097-0000-0000-df00-014105000000"
}
```
