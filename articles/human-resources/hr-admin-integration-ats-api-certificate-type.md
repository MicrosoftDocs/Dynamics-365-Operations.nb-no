---
title: Attesttype
description: Dette emnet beskriver Sertifikattype-enheten for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1d2d53a628ef43d50bd83fd6b62807f44eddd653
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2021
ms.locfileid: "5125719"
---
# <a name="certificate-type"></a><span data-ttu-id="97b8f-103">Attesttype</span><span class="sxs-lookup"><span data-stu-id="97b8f-103">Certificate type</span></span>

<span data-ttu-id="97b8f-104">Dette emnet beskriver Sertifikattype-enheten for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="97b8f-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="97b8f-105">Fysisk navn: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="97b8f-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="97b8f-106">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="97b8f-106">Description</span></span>

<span data-ttu-id="97b8f-107">Denne enheten definerer listen over profesjonelle sertifikattyper som er definert i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="97b8f-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="97b8f-108">Enheten er ikke spesifikk for en juridisk enhet (firma).</span><span class="sxs-lookup"><span data-stu-id="97b8f-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="97b8f-109">JSON-representasjon</span><span class="sxs-lookup"><span data-stu-id="97b8f-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="97b8f-110">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="97b8f-110">Properties</span></span>

| <span data-ttu-id="97b8f-111">Egenskap</span><span class="sxs-lookup"><span data-stu-id="97b8f-111">Property</span></span><br><span data-ttu-id="97b8f-112">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="97b8f-112">**Physical name**</span></span><br><span data-ttu-id="97b8f-113">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="97b8f-113">**_Type_**</span></span> | <span data-ttu-id="97b8f-114">Bruk</span><span class="sxs-lookup"><span data-stu-id="97b8f-114">Use</span></span> | <span data-ttu-id="97b8f-115">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="97b8f-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="97b8f-116">**ID for Sertifikattype-enhet**</span><span class="sxs-lookup"><span data-stu-id="97b8f-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="97b8f-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="97b8f-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="97b8f-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="97b8f-118">*GUID*</span></span> | <span data-ttu-id="97b8f-119">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="97b8f-119">Read-only</span></span><br><span data-ttu-id="97b8f-120">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="97b8f-120">Required</span></span> 
<span data-ttu-id="97b8f-121">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="97b8f-121">System-generated</span></span> | <span data-ttu-id="97b8f-122">Unik primær identifikator for sertifikattypen.</span><span class="sxs-lookup"><span data-stu-id="97b8f-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="97b8f-123">**Sertifikattype**</span><span class="sxs-lookup"><span data-stu-id="97b8f-123">**Certificate Type**</span></span><br><span data-ttu-id="97b8f-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="97b8f-124">mshr_certificatetype</span></span><br><span data-ttu-id="97b8f-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="97b8f-125">*String*</span></span> | <span data-ttu-id="97b8f-126">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="97b8f-126">Read/write</span></span><br><span data-ttu-id="97b8f-127">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="97b8f-127">Required</span></span> | <span data-ttu-id="97b8f-128">Unik brukerlesbare identifikator for sertifikattypen.</span><span class="sxs-lookup"><span data-stu-id="97b8f-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="97b8f-129">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="97b8f-129">**Description**</span></span><br><span data-ttu-id="97b8f-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="97b8f-130">mshr_description</span></span><br><span data-ttu-id="97b8f-131">*Streng*</span><span class="sxs-lookup"><span data-stu-id="97b8f-131">*String*</span></span> | <span data-ttu-id="97b8f-132">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="97b8f-132">Read/write</span></span><br><span data-ttu-id="97b8f-133">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="97b8f-133">Required</span></span> | <span data-ttu-id="97b8f-134">Beskrivelse av sertifikattypen.</span><span class="sxs-lookup"><span data-stu-id="97b8f-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="97b8f-135">**Krever fornying**</span><span class="sxs-lookup"><span data-stu-id="97b8f-135">**Require Renewal**</span></span><br><span data-ttu-id="97b8f-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="97b8f-136">mshr_requirerenewal</span></span><br><span data-ttu-id="97b8f-137">*mshr_noyes-alternativsett*</span><span class="sxs-lookup"><span data-stu-id="97b8f-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="97b8f-138">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="97b8f-138">Read/write</span></span><br><span data-ttu-id="97b8f-139">Valgfri</span><span class="sxs-lookup"><span data-stu-id="97b8f-139">Optional</span></span> | <span data-ttu-id="97b8f-140">Angir om det kreves fornyelse for sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="97b8f-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="97b8f-141">Se også</span><span class="sxs-lookup"><span data-stu-id="97b8f-141">See also</span></span>

[<span data-ttu-id="97b8f-142">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="97b8f-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="97b8f-143">Eksempelspørring for Kandidat for ansettelse</span><span class="sxs-lookup"><span data-stu-id="97b8f-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)

