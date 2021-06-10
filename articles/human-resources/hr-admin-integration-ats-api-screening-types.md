---
title: Screeningtyper
description: Dette emnet beskriver Screeningtyper-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 2acb99c2fb57df883ab376c7f6aab547073bd0ff
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6058302"
---
# <a name="screening-types"></a><span data-ttu-id="8ca27-103">Screeningtyper</span><span class="sxs-lookup"><span data-stu-id="8ca27-103">Screening types</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="8ca27-104">Dette emnet beskriver Screeningtyper-enheten for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="8ca27-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="8ca27-105">Fysisk navn: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="8ca27-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="8ca27-106">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8ca27-106">Description</span></span>

<span data-ttu-id="8ca27-107">Denne enheten beskriver screeningtypene som er definert av firmaet for screeningprosesser før ansettelse og nåværende ansatte.</span><span class="sxs-lookup"><span data-stu-id="8ca27-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="8ca27-108">JSON-representasjon</span><span class="sxs-lookup"><span data-stu-id="8ca27-108">JSON representation</span></span>

```json
{
    "mshr_description": "String",
    "mshr_frequencyunit": Int,
    "mshr_generatefrom": Int,
    "mshr_frequencyinterval": Int,
    "mshr_screeningtypeid": "String",
    "mshr_hcmscreeningtypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="8ca27-109">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="8ca27-109">Properties</span></span>

| <span data-ttu-id="8ca27-110">Egenskap</span><span class="sxs-lookup"><span data-stu-id="8ca27-110">Property</span></span><br><span data-ttu-id="8ca27-111">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="8ca27-111">**Physical name**</span></span><br><span data-ttu-id="8ca27-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="8ca27-112">**_Type_**</span></span> | <span data-ttu-id="8ca27-113">Bruk</span><span class="sxs-lookup"><span data-stu-id="8ca27-113">Use</span></span> | <span data-ttu-id="8ca27-114">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="8ca27-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="8ca27-115">**ID for Screeningtype-enhet**</span><span class="sxs-lookup"><span data-stu-id="8ca27-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="8ca27-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="8ca27-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="8ca27-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="8ca27-117">*GUID*</span></span> | <span data-ttu-id="8ca27-118">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="8ca27-118">Read-only</span></span><br><span data-ttu-id="8ca27-119">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="8ca27-119">Required</span></span><br><span data-ttu-id="8ca27-120">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="8ca27-120">System-generated</span></span> | <span data-ttu-id="8ca27-121">Unik primær-ID for posten for screeningtype.</span><span class="sxs-lookup"><span data-stu-id="8ca27-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="8ca27-122">**ID for screeningtype**</span><span class="sxs-lookup"><span data-stu-id="8ca27-122">**Screening Type ID**</span></span><br><span data-ttu-id="8ca27-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="8ca27-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="8ca27-124">*Streng*</span><span class="sxs-lookup"><span data-stu-id="8ca27-124">*String*</span></span> | <span data-ttu-id="8ca27-125">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="8ca27-125">Read/write</span></span><br><span data-ttu-id="8ca27-126">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="8ca27-126">Required</span></span> | <span data-ttu-id="8ca27-127">Brukerdefinert unik identifikator for screeningtype.</span><span class="sxs-lookup"><span data-stu-id="8ca27-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="8ca27-128">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="8ca27-128">**Description**</span></span><br><span data-ttu-id="8ca27-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="8ca27-129">mshr_description</span></span><br><span data-ttu-id="8ca27-130">*Streng*</span><span class="sxs-lookup"><span data-stu-id="8ca27-130">*String*</span></span> | <span data-ttu-id="8ca27-131">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="8ca27-131">Read/write</span></span><br><span data-ttu-id="8ca27-132">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="8ca27-132">Required</span></span> | <span data-ttu-id="8ca27-133">Beskrivelse av screeningtypen.</span><span class="sxs-lookup"><span data-stu-id="8ca27-133">The description of the screening type.</span></span> |
| <span data-ttu-id="8ca27-134">**Frekvensenhet**</span><span class="sxs-lookup"><span data-stu-id="8ca27-134">**Frequency Unit**</span></span><br><span data-ttu-id="8ca27-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="8ca27-135">mshr_frequencyunit</span></span><br><span data-ttu-id="8ca27-136">*mshr_hcmfrequencyunit-alternativsett*</span><span class="sxs-lookup"><span data-stu-id="8ca27-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="8ca27-137">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="8ca27-137">Read/write</span></span><br><span data-ttu-id="8ca27-138">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="8ca27-138">Required</span></span> | <span data-ttu-id="8ca27-139">Beskriver hvor ofte screeningen må fullføres for den tilordnede personen.</span><span class="sxs-lookup"><span data-stu-id="8ca27-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="8ca27-140">**Generer fra**</span><span class="sxs-lookup"><span data-stu-id="8ca27-140">**Generate From**</span></span><br><span data-ttu-id="8ca27-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="8ca27-141">mshr_generatefrom</span></span><br><span data-ttu-id="8ca27-142">*mshr_hcmfrequencygeneratefrom-alternativsett*</span><span class="sxs-lookup"><span data-stu-id="8ca27-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="8ca27-143">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="8ca27-143">Read-write</span></span><br><span data-ttu-id="8ca27-144">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="8ca27-144">Required</span></span> | <span data-ttu-id="8ca27-145">Hvis frekvensverdien er en annen verdi enn "Bare én gang", bestemmer GenerateFrom-verdien datoen som neste screeninghendelse skal beregnes fra.</span><span class="sxs-lookup"><span data-stu-id="8ca27-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="8ca27-146">**Frekvensintervall**</span><span class="sxs-lookup"><span data-stu-id="8ca27-146">**Frequency Interval**</span></span><br><span data-ttu-id="8ca27-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="8ca27-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="8ca27-148">*Heltall*</span><span class="sxs-lookup"><span data-stu-id="8ca27-148">*Integer*</span></span> | <span data-ttu-id="8ca27-149">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="8ca27-149">Read-write</span></span><br><span data-ttu-id="8ca27-150">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="8ca27-150">Required</span></span> | <span data-ttu-id="8ca27-151">Hvis frekvensverdien er en annen verdi enn "Bare én gang", må du definere et intervall for tidsenhetene mellom hver screeninghendelse.</span><span class="sxs-lookup"><span data-stu-id="8ca27-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="8ca27-152">Se også</span><span class="sxs-lookup"><span data-stu-id="8ca27-152">See also</span></span>

[<span data-ttu-id="8ca27-153">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="8ca27-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="8ca27-154">Eksempelspørring for Kandidat for ansettelse</span><span class="sxs-lookup"><span data-stu-id="8ca27-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]