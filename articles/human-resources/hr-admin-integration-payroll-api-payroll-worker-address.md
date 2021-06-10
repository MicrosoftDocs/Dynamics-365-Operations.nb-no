---
title: Adresse til lønnsarbeider
description: Dette emnet inneholder informasjon og en eksempelspørring for Adresse til lønnsarbeider-enheten i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3407128b0172f0e253d51bcfa23a894f981e21e2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6052295"
---
# <a name="payroll-worker-address"></a><span data-ttu-id="942cf-103">Adresse til lønnsarbeider</span><span class="sxs-lookup"><span data-stu-id="942cf-103">Payroll worker address</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="942cf-104">Dette emnet inneholder informasjon og en eksempelspørring for Adresse til lønnsarbeider-enheten i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="942cf-104">This topic provides details and an example query for the Payroll worker address entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="942cf-105">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="942cf-105">Properties</span></span>

| <span data-ttu-id="942cf-106">Egenskap</span><span class="sxs-lookup"><span data-stu-id="942cf-106">Property</span></span><br><span data-ttu-id="942cf-107">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="942cf-107">**Physical name**</span></span><br><span data-ttu-id="942cf-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="942cf-108">**_Type_**</span></span> | <span data-ttu-id="942cf-109">Bruk</span><span class="sxs-lookup"><span data-stu-id="942cf-109">Use</span></span> | <span data-ttu-id="942cf-110">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="942cf-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="942cf-111">**Poststed**</span><span class="sxs-lookup"><span data-stu-id="942cf-111">**City**</span></span><br><span data-ttu-id="942cf-112">mshr_city</span><span class="sxs-lookup"><span data-stu-id="942cf-112">mshr_city</span></span><br><span data-ttu-id="942cf-113">*Streng*</span><span class="sxs-lookup"><span data-stu-id="942cf-113">*String*</span></span> | <span data-ttu-id="942cf-114">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="942cf-114">Read-only</span></span><br><span data-ttu-id="942cf-115">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="942cf-115">Required</span></span> | <span data-ttu-id="942cf-116">Poststedet definert for adressen.</span><span class="sxs-lookup"><span data-stu-id="942cf-116">The city defined for the address.</span></span>   |
| <span data-ttu-id="942cf-117">**Personalnummer**</span><span class="sxs-lookup"><span data-stu-id="942cf-117">**Personnel number**</span></span><br><span data-ttu-id="942cf-118">mshr_personnelnumber</span><span class="sxs-lookup"><span data-stu-id="942cf-118">mshr_personnelnumber</span></span><br><span data-ttu-id="942cf-119">*Streng*</span><span class="sxs-lookup"><span data-stu-id="942cf-119">*String*</span></span> | <span data-ttu-id="942cf-120">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="942cf-120">Read-only</span></span><br><span data-ttu-id="942cf-121">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="942cf-121">Required</span></span> | <span data-ttu-id="942cf-122">Det unike personalnummeret til den ansatte.</span><span class="sxs-lookup"><span data-stu-id="942cf-122">The employee's unique personnel number.</span></span>  |
| <span data-ttu-id="942cf-123">**Land/område**</span><span class="sxs-lookup"><span data-stu-id="942cf-123">**Country region**</span></span><br><span data-ttu-id="942cf-124">mshr_countryregionid</span><span class="sxs-lookup"><span data-stu-id="942cf-124">mshr_countryregionid</span></span><br><span data-ttu-id="942cf-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="942cf-125">*String*</span></span> | <span data-ttu-id="942cf-126">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="942cf-126">Read-only</span></span><br><span data-ttu-id="942cf-127">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="942cf-127">Required</span></span> | <span data-ttu-id="942cf-128">Landet eller området definert for adressen.</span><span class="sxs-lookup"><span data-stu-id="942cf-128">The country region defined for the address</span></span>  |
| <span data-ttu-id="942cf-129">**Gyldig fra**</span><span class="sxs-lookup"><span data-stu-id="942cf-129">**Valid from**</span></span><br><span data-ttu-id="942cf-130">mshr_postaladdressvalidfrom</span><span class="sxs-lookup"><span data-stu-id="942cf-130">mshr_postaladdressvalidfrom</span></span><br><span data-ttu-id="942cf-131">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="942cf-131">*Date Time Offset*</span></span> | <span data-ttu-id="942cf-132">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="942cf-132">Read-only</span></span> <br><span data-ttu-id="942cf-133">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="942cf-133">Required</span></span> | <span data-ttu-id="942cf-134">Datoen som adressen gjelder fra.</span><span class="sxs-lookup"><span data-stu-id="942cf-134">The date the address is valid from.</span></span> |
| <span data-ttu-id="942cf-135">**Arbeidet i adresse**</span><span class="sxs-lookup"><span data-stu-id="942cf-135">**Worked in address**</span></span><br><span data-ttu-id="942cf-136">mshr_isworkedinaddressbr>*Int32*</span><span class="sxs-lookup"><span data-stu-id="942cf-136">mshr_isworkedinaddressbr>*Int32*</span></span> | <span data-ttu-id="942cf-137">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="942cf-137">Read-only</span></span><br><span data-ttu-id="942cf-138">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="942cf-138">Required</span></span> | <span data-ttu-id="942cf-139">Angir om adressen er der den ansatte arbeider.</span><span class="sxs-lookup"><span data-stu-id="942cf-139">Denotes if the address is where the employee works.</span></span> |
| <span data-ttu-id="942cf-140">**Kommune**</span><span class="sxs-lookup"><span data-stu-id="942cf-140">**County**</span></span><br><span data-ttu-id="942cf-141">mshr_county</span><span class="sxs-lookup"><span data-stu-id="942cf-141">mshr_county</span></span><br><span data-ttu-id="942cf-142">*Streng*</span><span class="sxs-lookup"><span data-stu-id="942cf-142">*String*</span></span> | <span data-ttu-id="942cf-143">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="942cf-143">Read-only</span></span><br><span data-ttu-id="942cf-144">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="942cf-144">Required</span></span> | <span data-ttu-id="942cf-145">Landet definert for adressen.</span><span class="sxs-lookup"><span data-stu-id="942cf-145">The county defined for the address.</span></span>  |
| <span data-ttu-id="942cf-146">**Adresse-ID for lønnsarbeider**</span><span class="sxs-lookup"><span data-stu-id="942cf-146">**Payroll worker address ID**</span></span><br><span data-ttu-id="942cf-147">mshr_payrollworkeraddressentityid</span><span class="sxs-lookup"><span data-stu-id="942cf-147">mshr_payrollworkeraddressentityid</span></span><br><span data-ttu-id="942cf-148">*GUID*</span><span class="sxs-lookup"><span data-stu-id="942cf-148">*GUID*</span></span> | <span data-ttu-id="942cf-149">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="942cf-149">Required</span></span><br><span data-ttu-id="942cf-150">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="942cf-150">System generated</span></span> | <span data-ttu-id="942cf-151">En systemgenerert GUID-verdi som entydig identifiserer adressen.</span><span class="sxs-lookup"><span data-stu-id="942cf-151">A system-generated GUID value to uniquely identify the address.</span></span>  |
| <span data-ttu-id="942cf-152">**Primærfelt**</span><span class="sxs-lookup"><span data-stu-id="942cf-152">**Primary field**</span></span><br><span data-ttu-id="942cf-153">mshr_primaryfield</span><span class="sxs-lookup"><span data-stu-id="942cf-153">mshr_primaryfield</span></span><br><span data-ttu-id="942cf-154">*Streng*</span><span class="sxs-lookup"><span data-stu-id="942cf-154">*String*</span></span> | <span data-ttu-id="942cf-155">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="942cf-155">Read-only</span></span><br><span data-ttu-id="942cf-156">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="942cf-156">Required</span></span> |  |
| <span data-ttu-id="942cf-157">**Gate**</span><span class="sxs-lookup"><span data-stu-id="942cf-157">**Street**</span></span><br><span data-ttu-id="942cf-158">mshr_street</span><span class="sxs-lookup"><span data-stu-id="942cf-158">mshr_street</span></span><br><span data-ttu-id="942cf-159">*Streng*</span><span class="sxs-lookup"><span data-stu-id="942cf-159">*String*</span></span> | <span data-ttu-id="942cf-160">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="942cf-160">Read-only</span></span><br><span data-ttu-id="942cf-161">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="942cf-161">Required</span></span> | <span data-ttu-id="942cf-162">Gaten definert for adressen.</span><span class="sxs-lookup"><span data-stu-id="942cf-162">The street defined for the address.</span></span> |
| <span data-ttu-id="942cf-163">**Gyldig til**</span><span class="sxs-lookup"><span data-stu-id="942cf-163">**Valid to**</span></span><br><span data-ttu-id="942cf-164">mshr_postaladdressvalidto</span><span class="sxs-lookup"><span data-stu-id="942cf-164">mshr_postaladdressvalidto</span></span><br><span data-ttu-id="942cf-165">*Motregning av dato/klokkeslett*</span><span class="sxs-lookup"><span data-stu-id="942cf-165">*Date Time Offset*</span></span> | <span data-ttu-id="942cf-166">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="942cf-166">Read-only</span></span> <br><span data-ttu-id="942cf-167">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="942cf-167">Required</span></span> | <span data-ttu-id="942cf-168">Datoen som adressen gjelder til.</span><span class="sxs-lookup"><span data-stu-id="942cf-168">The date the address is valid to.</span></span>  |
| <span data-ttu-id="942cf-169">**Plasserings-ID**</span><span class="sxs-lookup"><span data-stu-id="942cf-169">**Location ID**</span></span><br><span data-ttu-id="942cf-170">mshr_locationidbr>*Streng*</span><span class="sxs-lookup"><span data-stu-id="942cf-170">mshr_locationidbr>*String*</span></span> | <span data-ttu-id="942cf-171">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="942cf-171">Read-only</span></span> <br><span data-ttu-id="942cf-172">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="942cf-172">Required</span></span> | <span data-ttu-id="942cf-173">ID-en for adressen.</span><span class="sxs-lookup"><span data-stu-id="942cf-173">The ID for the address.</span></span>  |
| <span data-ttu-id="942cf-174">**Postnummer**</span><span class="sxs-lookup"><span data-stu-id="942cf-174">**Postal code**</span></span><br><span data-ttu-id="942cf-175">mshr_zipcode</span><span class="sxs-lookup"><span data-stu-id="942cf-175">mshr_zipcode</span></span><br><span data-ttu-id="942cf-176">*Streng*</span><span class="sxs-lookup"><span data-stu-id="942cf-176">*String*</span></span> | <span data-ttu-id="942cf-177">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="942cf-177">Read-only</span></span> <br><span data-ttu-id="942cf-178">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="942cf-178">Required</span></span> |<span data-ttu-id="942cf-179">Identifikasjonsnummeret som er definert for den ansatte.</span><span class="sxs-lookup"><span data-stu-id="942cf-179">The identification number defined for the employee.</span></span>  |
| <span data-ttu-id="942cf-180">**Bodde i adresse**</span><span class="sxs-lookup"><span data-stu-id="942cf-180">**Lived in address**</span></span><br><span data-ttu-id="942cf-181">mshr_islivedinaddressbr>*Streng*</span><span class="sxs-lookup"><span data-stu-id="942cf-181">mshr_islivedinaddressbr>*String*</span></span> | <span data-ttu-id="942cf-182">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="942cf-182">Read-only</span></span><br><span data-ttu-id="942cf-183">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="942cf-183">Required</span></span> | <span data-ttu-id="942cf-184">Angir om adressen er der den ansatte bor.</span><span class="sxs-lookup"><span data-stu-id="942cf-184">Denotes if the address is where the employee lives.</span></span> |
| <span data-ttu-id="942cf-185">**Delstat**</span><span class="sxs-lookup"><span data-stu-id="942cf-185">**State**</span></span><br><span data-ttu-id="942cf-186">mshr_state</span><span class="sxs-lookup"><span data-stu-id="942cf-186">mshr_state</span></span><br><span data-ttu-id="942cf-187">*Streng*</span><span class="sxs-lookup"><span data-stu-id="942cf-187">*String*</span></span> | <span data-ttu-id="942cf-188">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="942cf-188">Read-only</span></span><br><span data-ttu-id="942cf-189">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="942cf-189">Required</span></span> | <span data-ttu-id="942cf-190">Delstaten definert for adressen.</span><span class="sxs-lookup"><span data-stu-id="942cf-190">The state defined for the address.</span></span>  |

## <a name="example-query"></a><span data-ttu-id="942cf-191">Eksempelspørring</span><span class="sxs-lookup"><span data-stu-id="942cf-191">Example query</span></span>

<span data-ttu-id="942cf-192">**Forespørsel**</span><span class="sxs-lookup"><span data-stu-id="942cf-192">**Request**</span></span>

```http
GET [Organizaton URI]/api/data/v9.1/mshr_payrollworkeraddressentities?$filter=mshr_personnelnumber eq @personnelnumber and mshr_postaladdressvalidfrom le @asofdate and mshr_postaladdressvalidto ge @asofdate&@personnelnumber='000041'&@asofdate=2021-04-01
```

<span data-ttu-id="942cf-193">**Svar**</span><span class="sxs-lookup"><span data-stu-id="942cf-193">**Response**</span></span>

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
