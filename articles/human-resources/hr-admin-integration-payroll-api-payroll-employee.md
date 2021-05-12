---
title: Lønnsansatt
description: Dette emnet inneholder informasjon og en eksempelspørring for Lønnsansatt-enheten i Dynamics 365 Human Resources.
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
ms.openlocfilehash: d3977b758f65875a36749a49459c2a81459a7b69
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882050"
---
# <a name="payroll-employee"></a><span data-ttu-id="42bd4-103">Lønnsansatt</span><span class="sxs-lookup"><span data-stu-id="42bd4-103">Payroll employee</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="42bd4-104">Dette emnet inneholder informasjon og en eksempelspørring for Lønnsansatt-enheten i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="42bd4-104">This topic provides details and an example query for the Payroll employee entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="42bd4-105">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="42bd4-105">Properties</span></span>

| <span data-ttu-id="42bd4-106">Egenskap</span><span class="sxs-lookup"><span data-stu-id="42bd4-106">Property</span></span><br><span data-ttu-id="42bd4-107">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="42bd4-107">**Physical name**</span></span><br><span data-ttu-id="42bd4-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="42bd4-108">**_Type_**</span></span> | <span data-ttu-id="42bd4-109">Bruk</span><span class="sxs-lookup"><span data-stu-id="42bd4-109">Use</span></span> | <span data-ttu-id="42bd4-110">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="42bd4-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="42bd4-111">**Personalnummer**</span><span class="sxs-lookup"><span data-stu-id="42bd4-111">**Personnel number**</span></span><br><span data-ttu-id="42bd4-112">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="42bd4-112">mshr_personnelnumber</span></span><br><span data-ttu-id="42bd4-113">*Streng*</span><span class="sxs-lookup"><span data-stu-id="42bd4-113">*String*</span></span> | <span data-ttu-id="42bd4-114">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="42bd4-114">Read-only</span></span><br><span data-ttu-id="42bd4-115">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-115">Required</span></span> | <span data-ttu-id="42bd4-116">Det unike personalnummeret til den ansatte.</span><span class="sxs-lookup"><span data-stu-id="42bd4-116">The employee's unique personnel number.</span></span> |
| <span data-ttu-id="42bd4-117">**Primærfelt**</span><span class="sxs-lookup"><span data-stu-id="42bd4-117">**Primary field**</span></span><br><span data-ttu-id="42bd4-118">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="42bd4-118">mshr_primaryfield</span></span><br><span data-ttu-id="42bd4-119">*Streng*</span><span class="sxs-lookup"><span data-stu-id="42bd4-119">*String*</span></span> | <span data-ttu-id="42bd4-120">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-120">Required</span></span><br><span data-ttu-id="42bd4-121">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="42bd4-121">System generated</span></span> |  |
| <span data-ttu-id="42bd4-122">**Etternavn**</span><span class="sxs-lookup"><span data-stu-id="42bd4-122">**Last name**</span></span><br><span data-ttu-id="42bd4-123">mshr_lastname</span><span class="sxs-lookup"><span data-stu-id="42bd4-123">mshr_lastname</span></span><br><span data-ttu-id="42bd4-124">*Streng*</span><span class="sxs-lookup"><span data-stu-id="42bd4-124">*String*</span></span> | <span data-ttu-id="42bd4-125">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="42bd4-125">Read only</span></span><br><span data-ttu-id="42bd4-126">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-126">Required</span></span> | <span data-ttu-id="42bd4-127">Ansattes etternavn.</span><span class="sxs-lookup"><span data-stu-id="42bd4-127">Employee last name.</span></span> |
| <span data-ttu-id="42bd4-128">**ID for juridisk enhet**</span><span class="sxs-lookup"><span data-stu-id="42bd4-128">**Legal entity ID**</span></span><br><span data-ttu-id="42bd4-129">mshr_legalentityID</span><span class="sxs-lookup"><span data-stu-id="42bd4-129">mshr_legalentityID</span></span><br><span data-ttu-id="42bd4-130">*Streng*</span><span class="sxs-lookup"><span data-stu-id="42bd4-130">*String*</span></span> | <span data-ttu-id="42bd4-131">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="42bd4-131">Read-only</span></span><br><span data-ttu-id="42bd4-132">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-132">Required</span></span> | <span data-ttu-id="42bd4-133">Angir den juridiske enheten (firmaet).</span><span class="sxs-lookup"><span data-stu-id="42bd4-133">Specifies the legal entity (company).</span></span> |
| <span data-ttu-id="42bd4-134">**Gyldig fra**</span><span class="sxs-lookup"><span data-stu-id="42bd4-134">**Valid from**</span></span><br><span data-ttu-id="42bd4-135">mshr_namevalidfrom</span><span class="sxs-lookup"><span data-stu-id="42bd4-135">mshr_namevalidfrom</span></span><br><span data-ttu-id="42bd4-136">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="42bd4-136">*Date Time Offset*</span></span> | <span data-ttu-id="42bd4-137">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="42bd4-137">Read-only</span></span> <br><span data-ttu-id="42bd4-138">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-138">Required</span></span> | <span data-ttu-id="42bd4-139">Datoen som ansattinformasjonen er gyldig fra.</span><span class="sxs-lookup"><span data-stu-id="42bd4-139">Date the employee information is valid from.</span></span>  |
| <span data-ttu-id="42bd4-140">**Kjønn**</span><span class="sxs-lookup"><span data-stu-id="42bd4-140">**Gender**</span></span><br><span data-ttu-id="42bd4-141">mshr_gender</span><span class="sxs-lookup"><span data-stu-id="42bd4-141">mshr_gender</span></span><br><span data-ttu-id="42bd4-142">*Int32*</span><span class="sxs-lookup"><span data-stu-id="42bd4-142">*Int32*</span></span> | <span data-ttu-id="42bd4-143">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="42bd4-143">Read-only</span></span><br><span data-ttu-id="42bd4-144">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-144">Required</span></span> | <span data-ttu-id="42bd4-145">Den ansattes kjønn.</span><span class="sxs-lookup"><span data-stu-id="42bd4-145">The employee's gender.</span></span> |
| <span data-ttu-id="42bd4-146">**Enhets-ID for lønnsansatt**</span><span class="sxs-lookup"><span data-stu-id="42bd4-146">**Payroll employee entity ID**</span></span><br><span data-ttu-id="42bd4-147">mshr_payrollemployeeentityid</span><span class="sxs-lookup"><span data-stu-id="42bd4-147">mshr_payrollemployeeentityid</span></span><br><span data-ttu-id="42bd4-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="42bd4-148">*GUID*</span></span> | <span data-ttu-id="42bd4-149">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-149">Required</span></span><br><span data-ttu-id="42bd4-150">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="42bd4-150">System generated</span></span> | <span data-ttu-id="42bd4-151">En systemgenerert GUID-verdi som entydig identifiserer den ansatte.</span><span class="sxs-lookup"><span data-stu-id="42bd4-151">A system-generated GUID value to uniquely identify the employee.</span></span> |
| <span data-ttu-id="42bd4-152">**Startdato for ansettelse**</span><span class="sxs-lookup"><span data-stu-id="42bd4-152">**Employment start date**</span></span><br><span data-ttu-id="42bd4-153">mshr_employmentstartdate</span><span class="sxs-lookup"><span data-stu-id="42bd4-153">mshr_employmentstartdate</span></span><br><span data-ttu-id="42bd4-154">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="42bd4-154">*Date time offset*</span></span> | <span data-ttu-id="42bd4-155">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="42bd4-155">Read-only</span></span><br><span data-ttu-id="42bd4-156">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-156">Required</span></span> | <span data-ttu-id="42bd4-157">Startdatoen for den ansattes ansettelse.</span><span class="sxs-lookup"><span data-stu-id="42bd4-157">The start date of the employee's employment.</span></span> |
| <span data-ttu-id="42bd4-158">**ID for Identifikasjonstype**</span><span class="sxs-lookup"><span data-stu-id="42bd4-158">**Identification type ID**</span></span><br><span data-ttu-id="42bd4-159">mshr_identificationtypeid</span><span class="sxs-lookup"><span data-stu-id="42bd4-159">mshr_identificationtypeid</span></span><br><span data-ttu-id="42bd4-160">*Streng*</span><span class="sxs-lookup"><span data-stu-id="42bd4-160">*String*</span></span> |<span data-ttu-id="42bd4-161">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="42bd4-161">Read-only</span></span><br><span data-ttu-id="42bd4-162">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-162">Required</span></span> | <span data-ttu-id="42bd4-163">Identifikasjonstypen som er definert for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="42bd4-163">The identification type defined for the employee.</span></span> |
| <span data-ttu-id="42bd4-164">**Sluttdato for ansettelse**</span><span class="sxs-lookup"><span data-stu-id="42bd4-164">**Employment end date**</span></span><br><span data-ttu-id="42bd4-165">mshr_employmentenddate</span><span class="sxs-lookup"><span data-stu-id="42bd4-165">mshr_employmentenddate</span></span><br><span data-ttu-id="42bd4-166">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="42bd4-166">*Date time offset*</span></span> | <span data-ttu-id="42bd4-167">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="42bd4-167">Read-only</span></span><br><span data-ttu-id="42bd4-168">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-168">Required</span></span> |<span data-ttu-id="42bd4-169">Sluttdatoen for den ansattes ansettelse.</span><span class="sxs-lookup"><span data-stu-id="42bd4-169">The end of the employee's employment.</span></span>  |
| <span data-ttu-id="42bd4-170">**Dataområde-ID**</span><span class="sxs-lookup"><span data-stu-id="42bd4-170">**Data area ID**</span></span><br><span data-ttu-id="42bd4-171">mshr_dataareaid_id</span><span class="sxs-lookup"><span data-stu-id="42bd4-171">mshr_dataareaid_id</span></span><br><span data-ttu-id="42bd4-172">*GUID*</span><span class="sxs-lookup"><span data-stu-id="42bd4-172">*GUID*</span></span> | <span data-ttu-id="42bd4-173">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-173">Required</span></span> <br><span data-ttu-id="42bd4-174">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="42bd4-174">System generated</span></span> | <span data-ttu-id="42bd4-175">Systemgenerert GUID-verdi som identifiserer den juridiske enheten (firmaet).</span><span class="sxs-lookup"><span data-stu-id="42bd4-175">System-generated GUID value identifying the legal entity (company).</span></span> |
| <span data-ttu-id="42bd4-176">**Gyldig til**</span><span class="sxs-lookup"><span data-stu-id="42bd4-176">**Valid to**</span></span><br><span data-ttu-id="42bd4-177">mshr_namevalidto</span><span class="sxs-lookup"><span data-stu-id="42bd4-177">mshr_namevalidto</span></span><br><span data-ttu-id="42bd4-178">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="42bd4-178">*Date Time Offset*</span></span> |  <span data-ttu-id="42bd4-179">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="42bd4-179">Read-only</span></span><br><span data-ttu-id="42bd4-180">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-180">Required</span></span> | <span data-ttu-id="42bd4-181">Datoen som ansattinformasjonen er gyldig til.</span><span class="sxs-lookup"><span data-stu-id="42bd4-181">Date the employee information is valid to.</span></span> |
| <span data-ttu-id="42bd4-182">**Fødselsdato**</span><span class="sxs-lookup"><span data-stu-id="42bd4-182">**Birth date**</span></span><br><span data-ttu-id="42bd4-183">mshr_birthdate</span><span class="sxs-lookup"><span data-stu-id="42bd4-183">mshr_birthdate</span></span><br><span data-ttu-id="42bd4-184">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="42bd4-184">*Date Time Offset*</span></span> | <span data-ttu-id="42bd4-185">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="42bd4-185">Read-only</span></span> <br><span data-ttu-id="42bd4-186">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-186">Required</span></span> | <span data-ttu-id="42bd4-187">Den ansattes fødselsdato.</span><span class="sxs-lookup"><span data-stu-id="42bd4-187">The employee's birth date</span></span> |
| <span data-ttu-id="42bd4-188">**Identifikasjonsnummer til**</span><span class="sxs-lookup"><span data-stu-id="42bd4-188">**Identification number to**</span></span><br><span data-ttu-id="42bd4-189">mshr_identificationnumber</span><span class="sxs-lookup"><span data-stu-id="42bd4-189">mshr_identificationnumber</span></span><br><span data-ttu-id="42bd4-190">*Streng*</span><span class="sxs-lookup"><span data-stu-id="42bd4-190">*String*</span></span> | <span data-ttu-id="42bd4-191">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="42bd4-191">Read-only</span></span> <br><span data-ttu-id="42bd4-192">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-192">Required</span></span> |<span data-ttu-id="42bd4-193">Identifikasjonsnummeret som er definert for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="42bd4-193">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="42bd4-194">**Fornavn**</span><span class="sxs-lookup"><span data-stu-id="42bd4-194">**First name**</span></span><br><span data-ttu-id="42bd4-195">mshr_firstname</span><span class="sxs-lookup"><span data-stu-id="42bd4-195">mshr_firstname</span></span><br><span data-ttu-id="42bd4-196">*Streng*</span><span class="sxs-lookup"><span data-stu-id="42bd4-196">*String*</span></span> | <span data-ttu-id="42bd4-197">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="42bd4-197">Read-only</span></span><br><span data-ttu-id="42bd4-198">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-198">Required</span></span> | <span data-ttu-id="42bd4-199">Ansattes fornavn.</span><span class="sxs-lookup"><span data-stu-id="42bd4-199">Employee first name.</span></span> |
| <span data-ttu-id="42bd4-200">**Mellomnavn**</span><span class="sxs-lookup"><span data-stu-id="42bd4-200">**Middle name**</span></span><br><span data-ttu-id="42bd4-201">mshr_middlename</span><span class="sxs-lookup"><span data-stu-id="42bd4-201">mshr_middlename</span></span><br><span data-ttu-id="42bd4-202">*Streng*</span><span class="sxs-lookup"><span data-stu-id="42bd4-202">*String*</span></span> | <span data-ttu-id="42bd4-203">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="42bd4-203">Read-only</span></span><br><span data-ttu-id="42bd4-204">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="42bd4-204">Required</span></span> |<span data-ttu-id="42bd4-205">Ansattes mellomnavn.</span><span class="sxs-lookup"><span data-stu-id="42bd4-205">Employee middle name.</span></span>  |

## <a name="example-query-for-payroll-employee"></a><span data-ttu-id="42bd4-206">Eksempelspørring for lønnsansatt</span><span class="sxs-lookup"><span data-stu-id="42bd4-206">Example query for Payroll employee</span></span>

<span data-ttu-id="42bd4-207">**Forespørsel**</span><span class="sxs-lookup"><span data-stu-id="42bd4-207">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollemployeeentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_identificationtypeid eq @idtype and mshr_namevalidfrom le @asofdate and mshr_namevalidto ge @asofdate&@personnelnumber='000041'&@idtype='SSN'&@asofdate=2021-04-01
```

<span data-ttu-id="42bd4-208">**Svar**</span><span class="sxs-lookup"><span data-stu-id="42bd4-208">**Response**</span></span>

```json
{
         "mshr_legalentityid": "USMF",
            "mshr_personnelnumber": "000041",
            "mshr_employmentstartdate": "2011-04-05T07:00:00Z",
            "mshr_employmentenddate": "2154-12-31T23:59:59Z",
            "mshr_firstname": "Cassie",
            "mshr_middlename": "Lassie",
            "mshr_lastname": "Hicks",
            "mshr_namevalidfrom": "2021-03-12T20:34:25Z",
            "mshr_namevalidto": "2154-12-31T23:59:59Z",
            "mshr_birthdate": "1987-09-12T00:00:00Z",
            "mshr_gender": 200000002,
            "mshr_identificationtypeid": "SSN",
            "mshr_identificationnumber": "888-99-9342",
            "mshr_dataareaid": "USMF",
            "mshr_primaryfield": "000041 | USMF | 4/5/2011 07:00:00 am",
            "_mshr_fk_worker_id_value": "000000ad-0000-0000-d5ff-004105000000",
            "_mshr_fk_employment_id_value": "00000d0d-0000-0000-0600-014105000000",
            "_mshr_fk_fixedcompplan_id_value": "0000029f-0000-0000-d5ff-004105000000",
            "mshr_payrollemployeeentityid": "00000d3c-0000-0000-d5ff-004105000000",
            "_mshr_dataareaid_id_value": null
}
```