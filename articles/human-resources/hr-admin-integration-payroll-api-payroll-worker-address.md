---
title: Adresse til lønnsarbeider
description: Dette emnet inneholder informasjon og en eksempelspørring for Adresse til lønnsarbeider-enheten i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 6d93c38b21e953446142fc32cc2a0911616ac61d
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882046"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="a6ac2-103">Adresse til lønnsarbeider</span><span class="sxs-lookup"><span data-stu-id="a6ac2-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a6ac2-104">Dette emnet inneholder informasjon og en eksempelspørring for Adresse til lønnsarbeider-enheten i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a6ac2-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="a6ac2-105">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="a6ac2-105">Properties</span></span>

| <span data-ttu-id="a6ac2-106">Egenskap</span><span class="sxs-lookup"><span data-stu-id="a6ac2-106">Property</span></span><br><span data-ttu-id="a6ac2-107">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-107">**Physical name**</span></span><br><span data-ttu-id="a6ac2-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-108">**_Type_**</span></span> | <span data-ttu-id="a6ac2-109">Bruk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-109">Use</span></span> | <span data-ttu-id="a6ac2-110">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a6ac2-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a6ac2-111">**Poststed**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-111">**City**</span></span><br><span data-ttu-id="a6ac2-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="a6ac2-112">mshr_city</span></span><br><span data-ttu-id="a6ac2-113">*Streng*</span><span class="sxs-lookup"><span data-stu-id="a6ac2-113">*String*</span></span> | <span data-ttu-id="a6ac2-114">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="a6ac2-114">Read-only</span></span><br><span data-ttu-id="a6ac2-115">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-115">Required</span></span> | <span data-ttu-id="a6ac2-116">Poststedet definert for adressen.</span><span class="sxs-lookup"><span data-stu-id="a6ac2-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="a6ac2-117">**Personalnummer**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-117">**Personnel number**</span></span><br><span data-ttu-id="a6ac2-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="a6ac2-118">mshr_personnelnumber</span></span><br><span data-ttu-id="a6ac2-119">*Streng*</span><span class="sxs-lookup"><span data-stu-id="a6ac2-119">*String*</span></span> | <span data-ttu-id="a6ac2-120">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="a6ac2-120">Read-only</span></span><br><span data-ttu-id="a6ac2-121">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-121">Required</span></span> | <span data-ttu-id="a6ac2-122">Det unike personalnummeret til den ansatte.</span><span class="sxs-lookup"><span data-stu-id="a6ac2-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="a6ac2-123">**Land/område**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-123">**Country region**</span></span><br><span data-ttu-id="a6ac2-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="a6ac2-124">mshr_countryregionid</span></span><br><span data-ttu-id="a6ac2-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="a6ac2-125">*String*</span></span> | <span data-ttu-id="a6ac2-126">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="a6ac2-126">Read-only</span></span><br><span data-ttu-id="a6ac2-127">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-127">Required</span></span> | <span data-ttu-id="a6ac2-128">Landet eller området definert for adressen.</span><span class="sxs-lookup"><span data-stu-id="a6ac2-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="a6ac2-129">**Gyldig fra**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-129">**Valid from**</span></span><br><span data-ttu-id="a6ac2-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="a6ac2-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="a6ac2-131">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="a6ac2-131">*Date Time Offset*</span></span> | <span data-ttu-id="a6ac2-132">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="a6ac2-132">Read-only</span></span> <br><span data-ttu-id="a6ac2-133">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-133">Required</span></span> | <span data-ttu-id="a6ac2-134">Datoen som adressen gjelder fra.</span><span class="sxs-lookup"><span data-stu-id="a6ac2-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="a6ac2-135">**Arbeidet i adresse**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-135">**Worked in address**</span></span><br><span data-ttu-id="a6ac2-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="a6ac2-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="a6ac2-137">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="a6ac2-137">Read-only</span></span><br><span data-ttu-id="a6ac2-138">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-138">Required</span></span> | <span data-ttu-id="a6ac2-139">Angir om adressen er der den ansatte arbeider.</span><span class="sxs-lookup"><span data-stu-id="a6ac2-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="a6ac2-140">**Kommune**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-140">**County**</span></span><br><span data-ttu-id="a6ac2-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="a6ac2-141">mshr_county</span></span><br><span data-ttu-id="a6ac2-142">*Streng*</span><span class="sxs-lookup"><span data-stu-id="a6ac2-142">*String*</span></span> | <span data-ttu-id="a6ac2-143">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="a6ac2-143">Read-only</span></span><br><span data-ttu-id="a6ac2-144">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-144">Required</span></span> | <span data-ttu-id="a6ac2-145">Landet definert for adressen.</span><span class="sxs-lookup"><span data-stu-id="a6ac2-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="a6ac2-146">**Adresse-ID for lønnsarbeider**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="a6ac2-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="a6ac2-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="a6ac2-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="a6ac2-148">*GUID*</span></span> | <span data-ttu-id="a6ac2-149">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-149">Required</span></span><br><span data-ttu-id="a6ac2-150">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="a6ac2-150">System generated</span></span> | <span data-ttu-id="a6ac2-151">En systemgenerert GUID-verdi som entydig identifiserer adressen.</span><span class="sxs-lookup"><span data-stu-id="a6ac2-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="a6ac2-152">**Primærfelt**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-152">**Primary field**</span></span><br><span data-ttu-id="a6ac2-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="a6ac2-153">mshr_primaryfield</span></span><br><span data-ttu-id="a6ac2-154">*Streng*</span><span class="sxs-lookup"><span data-stu-id="a6ac2-154">*String*</span></span> | <span data-ttu-id="a6ac2-155">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="a6ac2-155">Read-only</span></span><br><span data-ttu-id="a6ac2-156">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-156">Required</span></span> |  |
| <span data-ttu-id="a6ac2-157">**Gate**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-157">**Street**</span></span><br><span data-ttu-id="a6ac2-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="a6ac2-158">mshr_street</span></span><br><span data-ttu-id="a6ac2-159">*Streng*</span><span class="sxs-lookup"><span data-stu-id="a6ac2-159">*String*</span></span> | <span data-ttu-id="a6ac2-160">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="a6ac2-160">Read-only</span></span><br><span data-ttu-id="a6ac2-161">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-161">Required</span></span> | <span data-ttu-id="a6ac2-162">Gaten definert for adressen.</span><span class="sxs-lookup"><span data-stu-id="a6ac2-162">The street defined for the address.</span></span> |
| <span data-ttu-id="a6ac2-163">**Gyldig til**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-163">**Valid to**</span></span><br><span data-ttu-id="a6ac2-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="a6ac2-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="a6ac2-165">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="a6ac2-165">*Date Time Offset*</span></span> | <span data-ttu-id="a6ac2-166">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="a6ac2-166">Read-only</span></span> <br><span data-ttu-id="a6ac2-167">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-167">Required</span></span> | <span data-ttu-id="a6ac2-168">Datoen som adressen gjelder til.</span><span class="sxs-lookup"><span data-stu-id="a6ac2-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="a6ac2-169">**Plasserings-ID**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-169">**Location ID**</span></span><br><span data-ttu-id="a6ac2-170">mshr_locationidbr>*Streng*</span><span class="sxs-lookup"><span data-stu-id="a6ac2-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="a6ac2-171">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="a6ac2-171">Read-only</span></span> <br><span data-ttu-id="a6ac2-172">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-172">Required</span></span> | <span data-ttu-id="a6ac2-173">ID-en for adressen.</span><span class="sxs-lookup"><span data-stu-id="a6ac2-173">The ID for the address.</span></span>  |
| <span data-ttu-id="a6ac2-174">**Postnummer**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-174">**Postal code**</span></span><br><span data-ttu-id="a6ac2-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="a6ac2-175">mshr_zipcode</span></span><br><span data-ttu-id="a6ac2-176">*Streng*</span><span class="sxs-lookup"><span data-stu-id="a6ac2-176">*String*</span></span> | <span data-ttu-id="a6ac2-177">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="a6ac2-177">Read-only</span></span> <br><span data-ttu-id="a6ac2-178">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-178">Required</span></span> |<span data-ttu-id="a6ac2-179">Identifikasjonsnummeret som er definert for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="a6ac2-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="a6ac2-180">**Bodde i adresse**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-180">**Lived in address**</span></span><br><span data-ttu-id="a6ac2-181">mshr_islivedinaddressbr>*Streng*</span><span class="sxs-lookup"><span data-stu-id="a6ac2-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="a6ac2-182">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="a6ac2-182">Read-only</span></span><br><span data-ttu-id="a6ac2-183">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-183">Required</span></span> | <span data-ttu-id="a6ac2-184">Angir om adressen er der den ansatte bor.</span><span class="sxs-lookup"><span data-stu-id="a6ac2-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="a6ac2-185">**Delstat**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-185">**State**</span></span><br><span data-ttu-id="a6ac2-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="a6ac2-186">mshr_state</span></span><br><span data-ttu-id="a6ac2-187">*Streng*</span><span class="sxs-lookup"><span data-stu-id="a6ac2-187">*String*</span></span> | <span data-ttu-id="a6ac2-188">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="a6ac2-188">Read-only</span></span><br><span data-ttu-id="a6ac2-189">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="a6ac2-189">Required</span></span> | <span data-ttu-id="a6ac2-190">Delstaten definert for adressen.</span><span class="sxs-lookup"><span data-stu-id="a6ac2-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="a6ac2-191">Eksempelspørring</span><span class="sxs-lookup"><span data-stu-id="a6ac2-191">Example query</span></span>

<span data-ttu-id="a6ac2-192">**Forespørsel**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="a6ac2-193">**Svar**</span><span class="sxs-lookup"><span data-stu-id="a6ac2-193">**Response**</span></span>

```json
{
            "mshr_personnelnumber": "000041",
            "mshr_locationid": "000000538",
            "mshr_islivedinaddress": 200000001,
            "mshr_isworkedinaddress": 200000000,
            "mshr_countryregionid": "USA",
            "mshr_zipcode": "99025",
            "mshr_street": "6543 Cypress Ave",
            "mshr_city": "Tacoma",
            "mshr_state": "WA",
            "mshr_county": "KING",
            "mshr_postaladdressvalidfrom": "2012-09-20T20:14:27Z",
            "mshr_postaladdressvalidto": "2154-12-31T23:59:59Z",
            "mshr_primaryfield": "000041 | 000000538 | 9/20/2012 08:14:27 pm",
            "_mshr_fk_worker_id_value": "00000d3c-0000-0000-d5ff-004105000000",
            "mshr_payrollworkeraddressentityid": "000006f0-0000-0000-f90f-014105000000"

}
```
