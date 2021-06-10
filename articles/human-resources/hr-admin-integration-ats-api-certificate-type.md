---
title: Attesttype
description: Dette emnet beskriver Sertifikattype-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: b8e979f242eb689b730b7f8a8684b3e697adbee6
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054698"
---
# <a name="certificate-type"></a><span data-ttu-id="4d5ce-103">Attesttype</span><span class="sxs-lookup"><span data-stu-id="4d5ce-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="4d5ce-104">Dette emnet beskriver Sertifikattype-enheten for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4d5ce-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="4d5ce-105">Fysisk navn: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="4d5ce-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="4d5ce-106">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="4d5ce-106">Description</span></span>

<span data-ttu-id="4d5ce-107">Denne enheten definerer listen over profesjonelle sertifikattyper som er definert i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="4d5ce-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="4d5ce-108">Enheten er ikke spesifikk for en juridisk enhet (firma).</span><span class="sxs-lookup"><span data-stu-id="4d5ce-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="4d5ce-109">JSON-representasjon</span><span class="sxs-lookup"><span data-stu-id="4d5ce-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="4d5ce-110">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="4d5ce-110">Properties</span></span>

| <span data-ttu-id="4d5ce-111">Egenskap</span><span class="sxs-lookup"><span data-stu-id="4d5ce-111">Property</span></span><br><span data-ttu-id="4d5ce-112">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="4d5ce-112">**Physical name**</span></span><br><span data-ttu-id="4d5ce-113">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="4d5ce-113">**_Type_**</span></span> | <span data-ttu-id="4d5ce-114">Bruk</span><span class="sxs-lookup"><span data-stu-id="4d5ce-114">Use</span></span> | <span data-ttu-id="4d5ce-115">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="4d5ce-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="4d5ce-116">**ID for Sertifikattype-enhet**</span><span class="sxs-lookup"><span data-stu-id="4d5ce-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="4d5ce-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="4d5ce-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="4d5ce-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="4d5ce-118">*GUID*</span></span> | <span data-ttu-id="4d5ce-119">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="4d5ce-119">Read-only</span></span><br><span data-ttu-id="4d5ce-120">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="4d5ce-120">Required</span></span> 
<span data-ttu-id="4d5ce-121">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="4d5ce-121">System-generated</span></span> | <span data-ttu-id="4d5ce-122">Unik primær identifikator for sertifikattypen.</span><span class="sxs-lookup"><span data-stu-id="4d5ce-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="4d5ce-123">**Sertifikattype**</span><span class="sxs-lookup"><span data-stu-id="4d5ce-123">**Certificate Type**</span></span><br><span data-ttu-id="4d5ce-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="4d5ce-124">mshr_certificatetype</span></span><br><span data-ttu-id="4d5ce-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="4d5ce-125">*String*</span></span> | <span data-ttu-id="4d5ce-126">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="4d5ce-126">Read/write</span></span><br><span data-ttu-id="4d5ce-127">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="4d5ce-127">Required</span></span> | <span data-ttu-id="4d5ce-128">Unik brukerlesbare identifikator for sertifikattypen.</span><span class="sxs-lookup"><span data-stu-id="4d5ce-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="4d5ce-129">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="4d5ce-129">**Description**</span></span><br><span data-ttu-id="4d5ce-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="4d5ce-130">mshr_description</span></span><br><span data-ttu-id="4d5ce-131">*Streng*</span><span class="sxs-lookup"><span data-stu-id="4d5ce-131">*String*</span></span> | <span data-ttu-id="4d5ce-132">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="4d5ce-132">Read/write</span></span><br><span data-ttu-id="4d5ce-133">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="4d5ce-133">Required</span></span> | <span data-ttu-id="4d5ce-134">Beskrivelse av sertifikattypen.</span><span class="sxs-lookup"><span data-stu-id="4d5ce-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="4d5ce-135">**Krever fornying**</span><span class="sxs-lookup"><span data-stu-id="4d5ce-135">**Require Renewal**</span></span><br><span data-ttu-id="4d5ce-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="4d5ce-136">mshr_requirerenewal</span></span><br><span data-ttu-id="4d5ce-137">*mshr_noyes-alternativsett*</span><span class="sxs-lookup"><span data-stu-id="4d5ce-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="4d5ce-138">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="4d5ce-138">Read/write</span></span><br><span data-ttu-id="4d5ce-139">Valgfri</span><span class="sxs-lookup"><span data-stu-id="4d5ce-139">Optional</span></span> | <span data-ttu-id="4d5ce-140">Angir om det kreves fornyelse for sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="4d5ce-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="4d5ce-141">Se også</span><span class="sxs-lookup"><span data-stu-id="4d5ce-141">See also</span></span>

[<span data-ttu-id="4d5ce-142">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="4d5ce-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="4d5ce-143">Eksempelspørring for Kandidat for ansettelse</span><span class="sxs-lookup"><span data-stu-id="4d5ce-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]