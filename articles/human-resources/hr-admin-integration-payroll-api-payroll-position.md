---
title: Lønnsdetaljer for stillinger
description: Dette emnet inneholder informasjon og en eksempelspørring for lønnsdetaljene for Stillinger-enheten i Dynamics 365 Human Resources.
author: jcart
manager: tfehr
ms.date: 04/07/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jcart
ms.search.validFrom: 2021-04-07
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f6c4bb0e2f4521e8c870f6c4fb645e2ce506138c
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882044"
---
# <a name="payroll-position"></a><span data-ttu-id="de6ed-103">Lønnsstilling</span><span class="sxs-lookup"><span data-stu-id="de6ed-103">Payroll position</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="de6ed-104">Dette emnet inneholder informasjon og en eksempelspørring for lønnsdetaljene for Stillinger-enheten i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="de6ed-104">This topic provides details and an example query for the Payroll details for the Positions entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="de6ed-105">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="de6ed-105">Properties</span></span>

| <span data-ttu-id="de6ed-106">Egenskap</span><span class="sxs-lookup"><span data-stu-id="de6ed-106">Property</span></span><br><span data-ttu-id="de6ed-107">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="de6ed-107">**Physical name**</span></span><br><span data-ttu-id="de6ed-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="de6ed-108">**_Type_**</span></span> | <span data-ttu-id="de6ed-109">Bruk</span><span class="sxs-lookup"><span data-stu-id="de6ed-109">Use</span></span> | <span data-ttu-id="de6ed-110">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="de6ed-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="de6ed-111">**Årlige vanlige timer**</span><span class="sxs-lookup"><span data-stu-id="de6ed-111">**Annual regular hours**</span></span><br><span data-ttu-id="de6ed-112">annualregularhours</span><span class="sxs-lookup"><span data-stu-id="de6ed-112">annualregularhours</span></span><br><span data-ttu-id="de6ed-113">*Desimal*</span><span class="sxs-lookup"><span data-stu-id="de6ed-113">*Decimal*</span></span> | <span data-ttu-id="de6ed-114">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="de6ed-114">Read-only</span></span><br><span data-ttu-id="de6ed-115">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="de6ed-115">Required</span></span> | <span data-ttu-id="de6ed-116">Årlige faste timer definert i stillingen.</span><span class="sxs-lookup"><span data-stu-id="de6ed-116">Annual regular hours defined on the position.</span></span>  |
| <span data-ttu-id="de6ed-117">**Enhets-ID for lønnsstillingsdetaljer**</span><span class="sxs-lookup"><span data-stu-id="de6ed-117">**Payroll position details entity ID**</span></span><br><span data-ttu-id="de6ed-118">payrollpositiondetailsentityid</span><span class="sxs-lookup"><span data-stu-id="de6ed-118">payrollpositiondetailsentityid</span></span><br><span data-ttu-id="de6ed-119">*Guid*</span><span class="sxs-lookup"><span data-stu-id="de6ed-119">*Guid*</span></span> | <span data-ttu-id="de6ed-120">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="de6ed-120">Required</span></span><br><span data-ttu-id="de6ed-121">Systemgenerert.</span><span class="sxs-lookup"><span data-stu-id="de6ed-121">System generated.</span></span> | <span data-ttu-id="de6ed-122">En systemgenerert GUID-verdi som entydig identifiserer stillingen.</span><span class="sxs-lookup"><span data-stu-id="de6ed-122">A system-generated GUID value to uniquely identify the position.</span></span>  |
| <span data-ttu-id="de6ed-123">**Primærfelt**</span><span class="sxs-lookup"><span data-stu-id="de6ed-123">**Primary field**</span></span><br><span data-ttu-id="de6ed-124">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="de6ed-124">mshr_primaryfield</span></span><br><span data-ttu-id="de6ed-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="de6ed-125">*String*</span></span> | <span data-ttu-id="de6ed-126">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="de6ed-126">Required</span></span><br><span data-ttu-id="de6ed-127">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="de6ed-127">System generated</span></span> |  |
| <span data-ttu-id="de6ed-128">**ID-verdi for stillingsjobb**</span><span class="sxs-lookup"><span data-stu-id="de6ed-128">**Position job ID value**</span></span><br><span data-ttu-id="de6ed-129">_mshr_fk_positionjob_id_value</span><span class="sxs-lookup"><span data-stu-id="de6ed-129">_mshr_fk_positionjob_id_value</span></span><br><span data-ttu-id="de6ed-130">*GUID*</span><span class="sxs-lookup"><span data-stu-id="de6ed-130">*GUID*</span></span> | <span data-ttu-id="de6ed-131">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="de6ed-131">Read-only</span></span><br><span data-ttu-id="de6ed-132">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="de6ed-132">Required</span></span><br><span data-ttu-id="de6ed-133">Sekundærnøkkel: mshr_PayrollPositionJobEntity av mshr_payrollpositionjobentity</span><span class="sxs-lookup"><span data-stu-id="de6ed-133">Foreign key:mshr_PayrollPositionJobEntity of the mshr_payrollpositionjobentity</span></span> |<span data-ttu-id="de6ed-134">ID-en for jobben som er knyttet til stillingen.</span><span class="sxs-lookup"><span data-stu-id="de6ed-134">The ID of the job associated with the position.</span></span>|
| <span data-ttu-id="de6ed-135">**ID-verdi for fast kompensasjonsplan**</span><span class="sxs-lookup"><span data-stu-id="de6ed-135">**Fixed compensation plan ID value**</span></span><br><span data-ttu-id="de6ed-136">_mshr_fk_fixedcompplan_id_value</span><span class="sxs-lookup"><span data-stu-id="de6ed-136">_mshr_fk_fixedcompplan_id_value</span></span><br><span data-ttu-id="de6ed-137">*GUID*</span><span class="sxs-lookup"><span data-stu-id="de6ed-137">*GUID*</span></span> | <span data-ttu-id="de6ed-138">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="de6ed-138">Read-only</span></span><br><span data-ttu-id="de6ed-139">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="de6ed-139">Required</span></span><br><span data-ttu-id="de6ed-140">Sekundærnøkkel: mshr_FixedCompPlan_id av mshr_payrollfixedcompensationplanentity</span><span class="sxs-lookup"><span data-stu-id="de6ed-140">Foreign key: mshr_FixedCompPlan_id of mshr_payrollfixedcompensationplanentity</span></span>  | <span data-ttu-id="de6ed-141">ID-en for den faste kompensasjonsplanen som er knyttet til stillingen.</span><span class="sxs-lookup"><span data-stu-id="de6ed-141">The ID of the fixed compensation plan associated with the position.</span></span> |
| <span data-ttu-id="de6ed-142">**ID for lønnssyklus**</span><span class="sxs-lookup"><span data-stu-id="de6ed-142">**Pay cycle ID**</span></span><br><span data-ttu-id="de6ed-143">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="de6ed-143">mshr_primaryfield</span></span><br><span data-ttu-id="de6ed-144">*Streng*</span><span class="sxs-lookup"><span data-stu-id="de6ed-144">*String*</span></span> | <span data-ttu-id="de6ed-145">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="de6ed-145">Read-only</span></span><br><span data-ttu-id="de6ed-146">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="de6ed-146">Required</span></span> | <span data-ttu-id="de6ed-147">Lønnssyklusen som er definert for stillingen.</span><span class="sxs-lookup"><span data-stu-id="de6ed-147">The pay cycle defined on the position.</span></span> |
| <span data-ttu-id="de6ed-148">**Betalt av juridisk enhet**</span><span class="sxs-lookup"><span data-stu-id="de6ed-148">**Paid by legal entity**</span></span><br><span data-ttu-id="de6ed-149">paidbylegalentity</span><span class="sxs-lookup"><span data-stu-id="de6ed-149">paidbylegalentity</span></span><br><span data-ttu-id="de6ed-150">*Streng*</span><span class="sxs-lookup"><span data-stu-id="de6ed-150">*String*</span></span> | <span data-ttu-id="de6ed-151">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="de6ed-151">Read-only</span></span><br><span data-ttu-id="de6ed-152">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="de6ed-152">Required</span></span> | <span data-ttu-id="de6ed-153">Den juridiske enheten som er definert i stillingen som er ansvarlig for utstedelse av betaling.</span><span class="sxs-lookup"><span data-stu-id="de6ed-153">The legal entity defined on the positoin responsible for issuing payment.</span></span> |
| <span data-ttu-id="de6ed-154">**Stillings-ID**</span><span class="sxs-lookup"><span data-stu-id="de6ed-154">**Position ID**</span></span><br><span data-ttu-id="de6ed-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="de6ed-155">mshr_positionid</span></span><br><span data-ttu-id="de6ed-156">*Streng*</span><span class="sxs-lookup"><span data-stu-id="de6ed-156">*String*</span></span> | <span data-ttu-id="de6ed-157">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="de6ed-157">Read-only</span></span><br><span data-ttu-id="de6ed-158">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="de6ed-158">Required</span></span> | <span data-ttu-id="de6ed-159">ID-en for stillingen.</span><span class="sxs-lookup"><span data-stu-id="de6ed-159">The ID of the position.</span></span> |
| <span data-ttu-id="de6ed-160">**Gyldig til**</span><span class="sxs-lookup"><span data-stu-id="de6ed-160">**Valid to**</span></span><br><span data-ttu-id="de6ed-161">validto</span><span class="sxs-lookup"><span data-stu-id="de6ed-161">validto</span></span><br><span data-ttu-id="de6ed-162">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="de6ed-162">*Date Time Offset*</span></span> | <span data-ttu-id="de6ed-163">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="de6ed-163">Read-only</span></span><br><span data-ttu-id="de6ed-164">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="de6ed-164">Required</span></span> |<span data-ttu-id="de6ed-165">Datoen stillingsdetaljene er gyldige fra.</span><span class="sxs-lookup"><span data-stu-id="de6ed-165">The date the position details are valid from.</span></span>  |
| <span data-ttu-id="de6ed-166">**Gyldig fra**</span><span class="sxs-lookup"><span data-stu-id="de6ed-166">**Valid from**</span></span><br><span data-ttu-id="de6ed-167">validfrom</span><span class="sxs-lookup"><span data-stu-id="de6ed-167">validfrom</span></span><br><span data-ttu-id="de6ed-168">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="de6ed-168">*Date Time Offset*</span></span> | <span data-ttu-id="de6ed-169">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="de6ed-169">Read-only</span></span><br><span data-ttu-id="de6ed-170">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="de6ed-170">Required</span></span> |<span data-ttu-id="de6ed-171">Datoen stillingsdetaljene er gyldige til.</span><span class="sxs-lookup"><span data-stu-id="de6ed-171">The date the position details are valid to.</span></span>  |

<span data-ttu-id="de6ed-172">**Forespørsel**</span><span class="sxs-lookup"><span data-stu-id="de6ed-172">**Query**</span></span>

<span data-ttu-id="de6ed-173">**Forespørsel**</span><span class="sxs-lookup"><span data-stu-id="de6ed-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollpositionentities?$filter=mshr_positionid eq @positionid and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@positionid='000276'&@asofdate=2021-04-01
```

<span data-ttu-id="de6ed-174">**Svar**</span><span class="sxs-lookup"><span data-stu-id="de6ed-174">**Response**</span></span>

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
