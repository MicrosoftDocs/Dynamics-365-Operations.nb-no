---
title: API for jobbdetaljer
description: Dette emnet inneholder informasjon og en eksempelspørring for Jobbdetalj-enheten i Dynamics 365 Human Resources.
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
ms.openlocfilehash: 4f15282bf72340cb1a832ff3264361472d0a6c70
ms.sourcegitcommit: d18d9cdb175c9d42eafbed66352c24b2aa94258b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/13/2021
ms.locfileid: "5882045"
---
# <a name="job-detail-api"></a><span data-ttu-id="68cec-103">API for jobbdetaljer</span><span class="sxs-lookup"><span data-stu-id="68cec-103">Job detail API</span></span>

<span data-ttu-id="68cec-104">Dette emnet inneholder informasjon og en eksempelspørring for Jobbdetalj-enheten i Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="68cec-104">This topic provides details and an example query for the Job detail entity in Dynamics 365 Human Resources.</span></span>

## <a name="properties"></a><span data-ttu-id="68cec-105">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="68cec-105">Properties</span></span>

| <span data-ttu-id="68cec-106">Egenskap</span><span class="sxs-lookup"><span data-stu-id="68cec-106">Property</span></span><br><span data-ttu-id="68cec-107">**Fysisk navn**</span><span class="sxs-lookup"><span data-stu-id="68cec-107">**Physical name**</span></span><br><span data-ttu-id="68cec-108">**_Type_**</span><span class="sxs-lookup"><span data-stu-id="68cec-108">**_Type_**</span></span> | <span data-ttu-id="68cec-109">Bruk</span><span class="sxs-lookup"><span data-stu-id="68cec-109">Use</span></span> | <span data-ttu-id="68cec-110">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="68cec-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="68cec-111">**Jobb-ID**</span><span class="sxs-lookup"><span data-stu-id="68cec-111">**Job ID**</span></span><br><span data-ttu-id="68cec-112">mshr_jobid</span><span class="sxs-lookup"><span data-stu-id="68cec-112">mshr_jobid</span></span><br><span data-ttu-id="68cec-113">*Streng*</span><span class="sxs-lookup"><span data-stu-id="68cec-113">*String*</span></span> | <span data-ttu-id="68cec-114">Skrivebeskyttet</span><span class="sxs-lookup"><span data-stu-id="68cec-114">Read-only</span></span><br><span data-ttu-id="68cec-115">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="68cec-115">Required</span></span> | <span data-ttu-id="68cec-116">Unik ID for en jobb.</span><span class="sxs-lookup"><span data-stu-id="68cec-116">Unique ID for a job.</span></span> |
| <span data-ttu-id="68cec-117">**Markedspris, lav terskel**</span><span class="sxs-lookup"><span data-stu-id="68cec-117">**Market price low threshold**</span></span><br><span data-ttu-id="68cec-118">mshr_marketpricelowthreshold</span><span class="sxs-lookup"><span data-stu-id="68cec-118">mshr_marketpricelowthreshold</span></span><br><span data-ttu-id="68cec-119">*Desimal*</span><span class="sxs-lookup"><span data-stu-id="68cec-119">*Decimal*</span></span> | | <span data-ttu-id="68cec-120">En systemgenerert GUID-verdi som entydig identifiserer stillingen.</span><span class="sxs-lookup"><span data-stu-id="68cec-120">A system-generated GUID value to uniquely identify the position.</span></span>  |
