---
title: Attesttype
description: Dette emnet beskriver Sertifikattype-enheten for Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.reviewer: anbichse
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: fe5713b6b5f38ad7f6857b36c6b2f63a1dc0c320
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798399"
---
# <a name="certificate-type"></a><span data-ttu-id="ae68b-103">Attesttype</span><span class="sxs-lookup"><span data-stu-id="ae68b-103">Certificate type</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ae68b-104">Dette emnet beskriver Sertifikattype-enheten for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ae68b-104">This topic describes the Certificate type entity for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ae68b-105">Fysisk navn: mshr_hcmcertificatetypeentity</span><span class="sxs-lookup"><span data-stu-id="ae68b-105">Physical name: mshr_hcmcertificatetypeentity</span></span>

## <a name="description"></a><span data-ttu-id="ae68b-106">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ae68b-106">Description</span></span>

<span data-ttu-id="ae68b-107">Denne enheten definerer listen over profesjonelle sertifikattyper som er definert i Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ae68b-107">This entity defines the list of professional certificate types set up in Human Resources.</span></span> <span data-ttu-id="ae68b-108">Enheten er ikke spesifikk for en juridisk enhet (firma).</span><span class="sxs-lookup"><span data-stu-id="ae68b-108">The entity isn't specific to a legal entity (company).</span></span>

## <a name="json-representation"></a><span data-ttu-id="ae68b-109">JSON-representasjon</span><span class="sxs-lookup"><span data-stu-id="ae68b-109">JSON representation</span></span>

```json
{
    "mshr_certificatetype": "String",
    "mshr_description": "String",
    "mshr_requirerenewal": Int,
    "mshr_hcmcertificatetypeentityid": "Guid"
}
```

## <a name="properties"></a><span data-ttu-id="ae68b-110">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="ae68b-110">Properties</span></span>

| <span data-ttu-id="ae68b-111">Egenskap</span><span class="sxs-lookup"><span data-stu-id="ae68b-111">Property</span></span><br><span data-ttu-id="ae68b-112">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="ae68b-112">**Physical name**</span></span><br><span data-ttu-id="ae68b-113">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="ae68b-113">**_Type_**</span></span> | <span data-ttu-id="ae68b-114">Bruk</span><span class="sxs-lookup"><span data-stu-id="ae68b-114">Use</span></span> | <span data-ttu-id="ae68b-115">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ae68b-115">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ae68b-116">**ID for Sertifikattype-enhet**</span><span class="sxs-lookup"><span data-stu-id="ae68b-116">**Certificate Type Entity ID**</span></span><br><span data-ttu-id="ae68b-117">mshr_hcmcertificatetypeentityid</span><span class="sxs-lookup"><span data-stu-id="ae68b-117">mshr_hcmcertificatetypeentityid</span></span><br><span data-ttu-id="ae68b-118">*GUID*</span><span class="sxs-lookup"><span data-stu-id="ae68b-118">*GUID*</span></span> | <span data-ttu-id="ae68b-119">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="ae68b-119">Read-only</span></span><br><span data-ttu-id="ae68b-120">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="ae68b-120">Required</span></span> 
<span data-ttu-id="ae68b-121">Systemgenerert</span><span class="sxs-lookup"><span data-stu-id="ae68b-121">System-generated</span></span> | <span data-ttu-id="ae68b-122">Unik primær identifikator for sertifikattypen.</span><span class="sxs-lookup"><span data-stu-id="ae68b-122">Unique primary identifier for the certificate type.</span></span> |
| <span data-ttu-id="ae68b-123">**Sertifikattype**</span><span class="sxs-lookup"><span data-stu-id="ae68b-123">**Certificate Type**</span></span><br><span data-ttu-id="ae68b-124">mshr_certificatetype</span><span class="sxs-lookup"><span data-stu-id="ae68b-124">mshr_certificatetype</span></span><br><span data-ttu-id="ae68b-125">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ae68b-125">*String*</span></span> | <span data-ttu-id="ae68b-126">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="ae68b-126">Read/write</span></span><br><span data-ttu-id="ae68b-127">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="ae68b-127">Required</span></span> | <span data-ttu-id="ae68b-128">Unik brukerlesbare identifikator for sertifikattypen.</span><span class="sxs-lookup"><span data-stu-id="ae68b-128">Unique user-readable identifier for the certificate type.</span></span> |
| <span data-ttu-id="ae68b-129">**Beskrivelse**</span><span class="sxs-lookup"><span data-stu-id="ae68b-129">**Description**</span></span><br><span data-ttu-id="ae68b-130">mshr_description</span><span class="sxs-lookup"><span data-stu-id="ae68b-130">mshr_description</span></span><br><span data-ttu-id="ae68b-131">*Streng*</span><span class="sxs-lookup"><span data-stu-id="ae68b-131">*String*</span></span> | <span data-ttu-id="ae68b-132">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="ae68b-132">Read/write</span></span><br><span data-ttu-id="ae68b-133">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="ae68b-133">Required</span></span> | <span data-ttu-id="ae68b-134">Beskrivelse av sertifikattypen.</span><span class="sxs-lookup"><span data-stu-id="ae68b-134">Description of the certificate type.</span></span> |
| <span data-ttu-id="ae68b-135">**Krever fornying**</span><span class="sxs-lookup"><span data-stu-id="ae68b-135">**Require Renewal**</span></span><br><span data-ttu-id="ae68b-136">mshr_requirerenewal</span><span class="sxs-lookup"><span data-stu-id="ae68b-136">mshr_requirerenewal</span></span><br><span data-ttu-id="ae68b-137">*mshr_noyes-alternativsett*</span><span class="sxs-lookup"><span data-stu-id="ae68b-137">*mshr_noyes option set*</span></span> | <span data-ttu-id="ae68b-138">Lese/skrive</span><span class="sxs-lookup"><span data-stu-id="ae68b-138">Read/write</span></span><br><span data-ttu-id="ae68b-139">Valgfri</span><span class="sxs-lookup"><span data-stu-id="ae68b-139">Optional</span></span> | <span data-ttu-id="ae68b-140">Angir om det kreves fornyelse for sertifikatet.</span><span class="sxs-lookup"><span data-stu-id="ae68b-140">Indicates whether renewal is required for the certificate.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ae68b-141">Se også</span><span class="sxs-lookup"><span data-stu-id="ae68b-141">See also</span></span>

[<span data-ttu-id="ae68b-142">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="ae68b-142">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ae68b-143">Eksempelspørring for Kandidat for ansettelse</span><span class="sxs-lookup"><span data-stu-id="ae68b-143">Example query for Candidate to hire</span></span>](hr-admin-integration-ats-api-candidate-to-hire-example-query.md)



[!INCLUDE[footer-include](../includes/footer-banner.md)]