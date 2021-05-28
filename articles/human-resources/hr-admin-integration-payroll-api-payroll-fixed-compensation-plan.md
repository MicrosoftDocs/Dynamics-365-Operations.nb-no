---
title: Fast kompensasjonsplan for lønn
description: Dette emnet inneholder informasjon og en eksempelspørring for enheten Fast kompensasjonsplan for lønn i Dynamics 365 Human Resources.
author: jcart
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
ms.openlocfilehash: 85cfce6f626090adab422ea6c60fc0778fd1ac67
ms.sourcegitcommit: 08ce2a9ca1f02064beabfb9b228717d39882164b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/11/2021
ms.locfileid: "6021302"
---
# <a name="payroll-fixed-compensation-plan"></a><span data-ttu-id="c4ccb-103">Fast kompensasjonsplan for lønn</span><span class="sxs-lookup"><span data-stu-id="c4ccb-103">Payroll fixed compensation plan</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c4ccb-104">Dette emnet inneholder informasjon og en eksempelspørring for enheten Fast kompensasjonsplan for lønn i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-104">This topic provides details and an example query for the Payroll fixed compensation plan entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="c4ccb-105">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="c4ccb-105">Properties</span></span>

| <span data-ttu-id="c4ccb-106">Egenskap</span><span class="sxs-lookup"><span data-stu-id="c4ccb-106">Property</span></span><br><span data-ttu-id="c4ccb-107">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-107">**Physical name**</span></span><br><span data-ttu-id="c4ccb-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-108">**_Type_**</span></span> | <span data-ttu-id="c4ccb-109">Bruk</span><span class="sxs-lookup"><span data-stu-id="c4ccb-109">Use</span></span> | <span data-ttu-id="c4ccb-110">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c4ccb-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c4ccb-111">**Ansatt-ID**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-111">**Employee ID**</span></span><br><span data-ttu-id="c4ccb-112">mshr_fk_employee_id_value</span><span class="sxs-lookup"><span data-stu-id="c4ccb-112">mshr_fk_employee_id_value</span></span><br><span data-ttu-id="c4ccb-113">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c4ccb-113">*GUID*</span></span> | <span data-ttu-id="c4ccb-114">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="c4ccb-114">Read-only</span></span><br><span data-ttu-id="c4ccb-115">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c4ccb-115">Required</span></span><br><span data-ttu-id="c4ccb-116">Sekundærnøkkel: mshr_Employee_id av mshr_payrollemployeeentity-enheten</span><span class="sxs-lookup"><span data-stu-id="c4ccb-116">Foreign key:mshr_Employee_id of mshr_payrollemployeeentity entity</span></span>  | <span data-ttu-id="c4ccb-117">Ansatt-ID</span><span class="sxs-lookup"><span data-stu-id="c4ccb-117">Employee ID</span></span> |
| <span data-ttu-id="c4ccb-118">**Lønnssats**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-118">**Pay rate**</span></span><br><span data-ttu-id="c4ccb-119">mshr_payrate</span><span class="sxs-lookup"><span data-stu-id="c4ccb-119">mshr_payrate</span></span><br><span data-ttu-id="c4ccb-120">*Desimal*</span><span class="sxs-lookup"><span data-stu-id="c4ccb-120">*Decimal*</span></span> | <span data-ttu-id="c4ccb-121">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="c4ccb-121">Read-only</span></span><br><span data-ttu-id="c4ccb-122">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c4ccb-122">Required</span></span> | <span data-ttu-id="c4ccb-123">Lønnssats som er definert i den faste kompensasjonsplanen.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-123">Pay rate defined in fixed compensation plan.</span></span> |
| <span data-ttu-id="c4ccb-124">**Plan-ID**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-124">**Plan ID**</span></span><br><span data-ttu-id="c4ccb-125">mshr_planid</span><span class="sxs-lookup"><span data-stu-id="c4ccb-125">mshr_planid</span></span><br><span data-ttu-id="c4ccb-126">*Streng*</span><span class="sxs-lookup"><span data-stu-id="c4ccb-126">*String*</span></span> | <span data-ttu-id="c4ccb-127">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="c4ccb-127">Read-only</span></span><br><span data-ttu-id="c4ccb-128">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c4ccb-128">Required</span></span> |<span data-ttu-id="c4ccb-129">Angir kompensasjonsplanen.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-129">Specifies the compensation plan.</span></span>  |
| <span data-ttu-id="c4ccb-130">**Gyldig fra**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-130">**Valid from**</span></span><br><span data-ttu-id="c4ccb-131">mshr_validfrom</span><span class="sxs-lookup"><span data-stu-id="c4ccb-131">mshr_validfrom</span></span><br><span data-ttu-id="c4ccb-132">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="c4ccb-132">*Date Time Offset*</span></span> |  <span data-ttu-id="c4ccb-133">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="c4ccb-133">Read-only</span></span><br><span data-ttu-id="c4ccb-134">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c4ccb-134">Required</span></span> |<span data-ttu-id="c4ccb-135">Datoen som den ansattes faste kompensasjon er gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-135">Date the employee fixed compensation is valid from.</span></span>  |
| <span data-ttu-id="c4ccb-136">**Fast kompensasjonsplan for lønn-enhet**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-136">**Payroll Fixed Compensation Plan entity**</span></span><br><span data-ttu-id="c4ccb-137">mshr_payrollfixedcompensationplanentityid</span><span class="sxs-lookup"><span data-stu-id="c4ccb-137">mshr_payrollfixedcompensationplanentityid</span></span><br><span data-ttu-id="c4ccb-138">*GUID*</span><span class="sxs-lookup"><span data-stu-id="c4ccb-138">*GUID*</span></span> | <span data-ttu-id="c4ccb-139">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c4ccb-139">Required</span></span><br><span data-ttu-id="c4ccb-140">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="c4ccb-140">Sytem generated</span></span> | <span data-ttu-id="c4ccb-141">En systemgenerert GUID-verdi som entydig identifiserer kompensasjonsplanen.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-141">A system-generated GUID value to uniquely identify the compensation plan.</span></span> |
| <span data-ttu-id="c4ccb-142">**Lønnsfrekvens**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-142">**Pay frequency**</span></span><br><span data-ttu-id="c4ccb-143">mshr_payfrequency</span><span class="sxs-lookup"><span data-stu-id="c4ccb-143">mshr_payfrequency</span></span><br><span data-ttu-id="c4ccb-144">*Streng*</span><span class="sxs-lookup"><span data-stu-id="c4ccb-144">*String*</span></span> | <span data-ttu-id="c4ccb-145">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="c4ccb-145">Read-only</span></span><br><span data-ttu-id="c4ccb-146">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c4ccb-146">Required</span></span> |<span data-ttu-id="c4ccb-147">Frekvensen den ansatte får betalt.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-147">The frequency the employee will be paid.</span></span>  |
| <span data-ttu-id="c4ccb-148">**Gyldig til**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-148">**Valid to**</span></span><br><span data-ttu-id="c4ccb-149">mshr_validto</span><span class="sxs-lookup"><span data-stu-id="c4ccb-149">mshr_validto</span></span><br><span data-ttu-id="c4ccb-150">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="c4ccb-150">*Date Time Offset*</span></span> | <span data-ttu-id="c4ccb-151">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="c4ccb-151">Read-only</span></span> <br><span data-ttu-id="c4ccb-152">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c4ccb-152">Required</span></span> | <span data-ttu-id="c4ccb-153">Datoen som den ansattes faste kompensasjon er gyldig til.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-153">Date the employee fixed compensation is valid to.</span></span> |
| <span data-ttu-id="c4ccb-154">**Stillings-ID**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-154">**Position ID**</span></span><br><span data-ttu-id="c4ccb-155">mshr_positionid</span><span class="sxs-lookup"><span data-stu-id="c4ccb-155">mshr_positionid</span></span><br><span data-ttu-id="c4ccb-156">*Streng*</span><span class="sxs-lookup"><span data-stu-id="c4ccb-156">*String*</span></span> | <span data-ttu-id="c4ccb-157">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="c4ccb-157">Read-only</span></span> <br><span data-ttu-id="c4ccb-158">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c4ccb-158">Required</span></span> | <span data-ttu-id="c4ccb-159">Posterings-ID som er knyttet til den ansatte og fast kompensasjonsplanregistrering.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-159">Postion ID associated with the employee and fixed compensation plan enrollment.</span></span> |
| <span data-ttu-id="c4ccb-160">**Valuta.**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-160">**Currency**</span></span><br><span data-ttu-id="c4ccb-161">mshr_currency</span><span class="sxs-lookup"><span data-stu-id="c4ccb-161">mshr_currency</span></span><br><span data-ttu-id="c4ccb-162">*Streng*</span><span class="sxs-lookup"><span data-stu-id="c4ccb-162">*String*</span></span> | <span data-ttu-id="c4ccb-163">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="c4ccb-163">Read-only</span></span> <br><span data-ttu-id="c4ccb-164">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c4ccb-164">Required</span></span> |<span data-ttu-id="c4ccb-165">Valutaen som er definert for den faste kompensasjonsplanen</span><span class="sxs-lookup"><span data-stu-id="c4ccb-165">The currency defined for the fixed compensation plan</span></span>   |
| <span data-ttu-id="c4ccb-166">**Personalnummer**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-166">**Personnel number**</span></span><br><span data-ttu-id="c4ccb-167">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="c4ccb-167">mshr_personnelnumber</span></span><br><span data-ttu-id="c4ccb-168">*Streng*</span><span class="sxs-lookup"><span data-stu-id="c4ccb-168">*String*</span></span> | <span data-ttu-id="c4ccb-169">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="c4ccb-169">Read-only</span></span><br><span data-ttu-id="c4ccb-170">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="c4ccb-170">Required</span></span> |<span data-ttu-id="c4ccb-171">Det unike personalnummeret til den ansatte.</span><span class="sxs-lookup"><span data-stu-id="c4ccb-171">The employee's unique personnel number.</span></span>  |

<span data-ttu-id="c4ccb-172">**Forespørsel**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-172">**Query**</span></span>

<span data-ttu-id="c4ccb-173">**Forespørsel**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-173">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollfixedcompensationplanentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_validfrom le @asofdate and mshr_validto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="c4ccb-174">**Svar**</span><span class="sxs-lookup"><span data-stu-id="c4ccb-174">**Response**</span></span>

```json
{
            "mshr_planid": "GradeC",
            "mshr_personnelnumber": "000041",
            "mshr_payrate": 75200,
            "mshr_positionid": "000276",
            "mshr_validfrom": "2011-04-05T00:00:00Z",
            "mshr_validto": "2154-12-31T00:00:00Z",
            "mshr_payfrequency": "Annual",
            "mshr_currency": "USD",
            "_mshr_fk_employee_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_fk_plan_id_value": "0000070c-0000-0000-b328-fef003000000",
            "_mshr_fk_job_id_value": "00010094-0000-0000-df00-014105000000",
            "mshr_payrollfixedcompensationplanentityid": "0000029f-0000-0000-d5ff-004105000000",
            "_mshr_fk_payroll_id_value": null
}
```
