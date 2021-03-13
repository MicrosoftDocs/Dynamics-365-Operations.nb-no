---
title: Screeningtyper
description: Dette emnet beskriver Screeningtyper-enheten for Dynamics 365 Human Resources.
author: jaredha
manager: tfehr
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.service: dynamics-365-human-resources
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 227c15acb44e020ea9858961e45c11ad07e18a74
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126176"
---
# <a name="screening-types"></a><span data-ttu-id="6330c-103">Screeningtyper</span><span class="sxs-lookup"><span data-stu-id="6330c-103">Screening types</span></span>

<span data-ttu-id="6330c-104">Dette emnet beskriver Screeningtyper-enheten for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="6330c-104">This topic describes the Screening types entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="6330c-105">Fysisk navn: mshr_hcmscreeningtypeentity</span><span class="sxs-lookup"><span data-stu-id="6330c-105">Physical name: mshr_hcmscreeningtypeentity</span></span>

## <a name="description"></a><span data-ttu-id="6330c-106">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6330c-106">Description</span></span>

<span data-ttu-id="6330c-107">Denne enheten beskriver screeningtypene som er definert av firmaet for screeningprosesser før ansettelse og nåværende ansatte.</span><span class="sxs-lookup"><span data-stu-id="6330c-107">This entity describes the screening types set up by the company for pre-employment and ongoing employee screening processes.</span></span>

## <a name="json-representation"></a><span data-ttu-id="6330c-108">JSON-representasjon</span><span class="sxs-lookup"><span data-stu-id="6330c-108">JSON representation</span></span>

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

## <a name="properties"></a><span data-ttu-id="6330c-109">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="6330c-109">Properties</span></span>

| <span data-ttu-id="6330c-110">Egenskap</span><span class="sxs-lookup"><span data-stu-id="6330c-110">Property</span></span><br><span data-ttu-id="6330c-111">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="6330c-111">**Physical name**</span></span><br><span data-ttu-id="6330c-112">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="6330c-112">**_Type_**</span></span> | <span data-ttu-id="6330c-113">Bruk</span><span class="sxs-lookup"><span data-stu-id="6330c-113">Use</span></span> | <span data-ttu-id="6330c-114">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="6330c-114">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="6330c-115">**ID for Screeningtype-enhet**</span><span class="sxs-lookup"><span data-stu-id="6330c-115">**Screening Type Entity ID**</span></span><br><span data-ttu-id="6330c-116">mshr_hcmscreeningtypeentityid</span><span class="sxs-lookup"><span data-stu-id="6330c-116">mshr_hcmscreeningtypeentityid</span></span><br><span data-ttu-id="6330c-117">*GUID*</span><span class="sxs-lookup"><span data-stu-id="6330c-117">*GUID*</span></span> | <span data-ttu-id="6330c-118">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="6330c-118">Read-only</span></span><br><span data-ttu-id="6330c-119">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="6330c-119">Required</span></span><br><span data-ttu-id="6330c-120">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="6330c-120">System-generated</span></span> | <span data-ttu-id="6330c-121">Unik primær-ID for posten for screeningtype.</span><span class="sxs-lookup"><span data-stu-id="6330c-121">Unique primary identifier for the screening type record.</span></span> |
| <span data-ttu-id="6330c-122">**ID for screeningtype**</span><span class="sxs-lookup"><span data-stu-id="6330c-122">**Screening Type ID**</span></span><br><span data-ttu-id="6330c-123">mshr_screeningtypeid</span><span class="sxs-lookup"><span data-stu-id="6330c-123">mshr_screeningtypeid</span></span><br><span data-ttu-id="6330c-124">*Streng*</span><span class="sxs-lookup"><span data-stu-id="6330c-124">*String*</span></span> | <span data-ttu-id="6330c-125">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="6330c-125">Read/write</span></span><br><span data-ttu-id="6330c-126">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="6330c-126">Required</span></span> | <span data-ttu-id="6330c-127">Brukerdefinert unik identifikator for screeningtype.</span><span class="sxs-lookup"><span data-stu-id="6330c-127">User-defined unique identifier for the screening type.</span></span> |
| <span data-ttu-id="6330c-128">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="6330c-128">**Description**</span></span><br><span data-ttu-id="6330c-129">mshr_description</span><span class="sxs-lookup"><span data-stu-id="6330c-129">mshr_description</span></span><br><span data-ttu-id="6330c-130">*Streng*</span><span class="sxs-lookup"><span data-stu-id="6330c-130">*String*</span></span> | <span data-ttu-id="6330c-131">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="6330c-131">Read/write</span></span><br><span data-ttu-id="6330c-132">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="6330c-132">Required</span></span> | <span data-ttu-id="6330c-133">Beskrivelse av screeningtypen.</span><span class="sxs-lookup"><span data-stu-id="6330c-133">The description of the screening type.</span></span> |
| <span data-ttu-id="6330c-134">**Frekvensenhet**</span><span class="sxs-lookup"><span data-stu-id="6330c-134">**Frequency Unit**</span></span><br><span data-ttu-id="6330c-135">mshr_frequencyunit</span><span class="sxs-lookup"><span data-stu-id="6330c-135">mshr_frequencyunit</span></span><br><span data-ttu-id="6330c-136">*mshr_hcmfrequencyunit-alternativsett*</span><span class="sxs-lookup"><span data-stu-id="6330c-136">*mshr_hcmfrequencyunit option set*</span></span> | <span data-ttu-id="6330c-137">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="6330c-137">Read/write</span></span><br><span data-ttu-id="6330c-138">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="6330c-138">Required</span></span> | <span data-ttu-id="6330c-139">Beskriver hvor ofte screeningen må fullføres for den tilordnede personen.</span><span class="sxs-lookup"><span data-stu-id="6330c-139">Describes the frequency with which the screening must be completed for the assigned person.</span></span> |
| <span data-ttu-id="6330c-140">**Generer fra**</span><span class="sxs-lookup"><span data-stu-id="6330c-140">**Generate From**</span></span><br><span data-ttu-id="6330c-141">mshr_generatefrom</span><span class="sxs-lookup"><span data-stu-id="6330c-141">mshr_generatefrom</span></span><br><span data-ttu-id="6330c-142">*mshr_hcmfrequencygeneratefrom-alternativsett*</span><span class="sxs-lookup"><span data-stu-id="6330c-142">*mshr_hcmfrequencygeneratefrom option set*</span></span> | <span data-ttu-id="6330c-143">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="6330c-143">Read-write</span></span><br><span data-ttu-id="6330c-144">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="6330c-144">Required</span></span> | <span data-ttu-id="6330c-145">Hvis frekvensverdien er en annen verdi enn "Bare én gang", bestemmer GenerateFrom-verdien datoen som neste screeninghendelse skal beregnes fra.</span><span class="sxs-lookup"><span data-stu-id="6330c-145">If the Frequency value is any value other than “One-time only”, the GenerateFrom value determines the date from which to calculate the next screening event.</span></span> |
| <span data-ttu-id="6330c-146">**Frekvensintervall**</span><span class="sxs-lookup"><span data-stu-id="6330c-146">**Frequency Interval**</span></span><br><span data-ttu-id="6330c-147">mshr_frequencyinterval</span><span class="sxs-lookup"><span data-stu-id="6330c-147">mshr_frequencyinterval</span></span><br><span data-ttu-id="6330c-148">*Heltall*</span><span class="sxs-lookup"><span data-stu-id="6330c-148">*Integer*</span></span> | <span data-ttu-id="6330c-149">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="6330c-149">Read-write</span></span><br><span data-ttu-id="6330c-150">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="6330c-150">Required</span></span> | <span data-ttu-id="6330c-151">Hvis frekvensverdien er en annen verdi enn "Bare én gang", må du definere et intervall for tidsenhetene mellom hver screeninghendelse.</span><span class="sxs-lookup"><span data-stu-id="6330c-151">If the Frequency value is any value other than “One-time only”, you must define an interval for the units of time between each screening event.</span></span> |

## <a name="see-also"></a><span data-ttu-id="6330c-152">Se også</span><span class="sxs-lookup"><span data-stu-id="6330c-152">See also</span></span>

[<span data-ttu-id="6330c-153">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="6330c-153">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="6330c-154">Eksempelspørring for Kandidat for ansettelse</span><span class="sxs-lookup"><span data-stu-id="6330c-154">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)
