---
title: Oversikt over MyLeaveRequests
description: MyLeaveRequests-enheten i Microsoft Dynamics 365 Human Resources gir listen over permisjonsforespørsler i systemet, begrenset til forespørslene som er tilgjengelige for den gjeldende brukeren som spør enheten.
author: andreabichsel
manager: tfehr
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-human-resources
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: c2c14a0cc935ad166a2c6600f1e96c3e09ab16ca
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5465516"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="286bd-103">Oversikt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="286bd-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="286bd-104">MyLeaveRequests-enheten i Microsoft Dynamics 365 Human Resources gir listen over permisjonsforespørsler i systemet, begrenset til forespørslene som er tilgjengelige for den gjeldende brukeren som spør enheten.</span><span class="sxs-lookup"><span data-stu-id="286bd-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="286bd-105">Nøkkel</span><span class="sxs-lookup"><span data-stu-id="286bd-105">Key</span></span>

  | <span data-ttu-id="286bd-106">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="286bd-106">Property Name</span></span> | <span data-ttu-id="286bd-107">Datatype</span><span class="sxs-lookup"><span data-stu-id="286bd-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="286bd-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="286bd-108">dataAreaId</span></span>    | <span data-ttu-id="286bd-109">Streng</span><span class="sxs-lookup"><span data-stu-id="286bd-109">String</span></span>    |
  | <span data-ttu-id="286bd-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="286bd-110">RequestId</span></span>     | <span data-ttu-id="286bd-111">Streng</span><span class="sxs-lookup"><span data-stu-id="286bd-111">String</span></span>    |
  | <span data-ttu-id="286bd-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="286bd-112">LeaveType</span></span>     | <span data-ttu-id="286bd-113">Streng</span><span class="sxs-lookup"><span data-stu-id="286bd-113">String</span></span>    |
  | <span data-ttu-id="286bd-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="286bd-114">LeaveDate</span></span>     | <span data-ttu-id="286bd-115">Dato</span><span class="sxs-lookup"><span data-stu-id="286bd-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="286bd-116">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="286bd-116">Properties</span></span>

  | <span data-ttu-id="286bd-117">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="286bd-117">Property Name</span></span>     | <span data-ttu-id="286bd-118">Datatype</span><span class="sxs-lookup"><span data-stu-id="286bd-118">Data Type</span></span> | <span data-ttu-id="286bd-119">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="286bd-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="286bd-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="286bd-120">dataAreaId</span></span>        | <span data-ttu-id="286bd-121">Streng</span><span class="sxs-lookup"><span data-stu-id="286bd-121">String</span></span>    | <span data-ttu-id="286bd-122">X</span><span class="sxs-lookup"><span data-stu-id="286bd-122">X</span></span>        |
  | <span data-ttu-id="286bd-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="286bd-123">RequestId</span></span>         | <span data-ttu-id="286bd-124">Streng</span><span class="sxs-lookup"><span data-stu-id="286bd-124">String</span></span>    | <span data-ttu-id="286bd-125">X</span><span class="sxs-lookup"><span data-stu-id="286bd-125">X</span></span>        |
  | <span data-ttu-id="286bd-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="286bd-126">LeaveType</span></span>         | <span data-ttu-id="286bd-127">Streng</span><span class="sxs-lookup"><span data-stu-id="286bd-127">String</span></span>    | <span data-ttu-id="286bd-128">X</span><span class="sxs-lookup"><span data-stu-id="286bd-128">X</span></span>        |
  | <span data-ttu-id="286bd-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="286bd-129">LeaveDate</span></span>         | <span data-ttu-id="286bd-130">Dato</span><span class="sxs-lookup"><span data-stu-id="286bd-130">Date</span></span>      | <span data-ttu-id="286bd-131">X</span><span class="sxs-lookup"><span data-stu-id="286bd-131">X</span></span>        |
  | <span data-ttu-id="286bd-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="286bd-132">ReasonCodeId</span></span>      | <span data-ttu-id="286bd-133">Streng</span><span class="sxs-lookup"><span data-stu-id="286bd-133">String</span></span>    |          |
  | <span data-ttu-id="286bd-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="286bd-134">PersonnelNumber</span></span>   | <span data-ttu-id="286bd-135">Streng</span><span class="sxs-lookup"><span data-stu-id="286bd-135">String</span></span>    | <span data-ttu-id="286bd-136">X</span><span class="sxs-lookup"><span data-stu-id="286bd-136">X</span></span>        |
  | <span data-ttu-id="286bd-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="286bd-137">RequestDate</span></span>       | <span data-ttu-id="286bd-138">Dato</span><span class="sxs-lookup"><span data-stu-id="286bd-138">Date</span></span>      | <span data-ttu-id="286bd-139">X</span><span class="sxs-lookup"><span data-stu-id="286bd-139">X</span></span>        |
  | <span data-ttu-id="286bd-140">Kommentar</span><span class="sxs-lookup"><span data-stu-id="286bd-140">Comment</span></span>           | <span data-ttu-id="286bd-141">Streng</span><span class="sxs-lookup"><span data-stu-id="286bd-141">String</span></span>    |          |
  | <span data-ttu-id="286bd-142">Status</span><span class="sxs-lookup"><span data-stu-id="286bd-142">Status</span></span>            | <span data-ttu-id="286bd-143">Opplisting</span><span class="sxs-lookup"><span data-stu-id="286bd-143">Enum</span></span>      | <span data-ttu-id="286bd-144">X</span><span class="sxs-lookup"><span data-stu-id="286bd-144">X</span></span>        |
  | <span data-ttu-id="286bd-145">Beløp</span><span class="sxs-lookup"><span data-stu-id="286bd-145">Amount</span></span>            | <span data-ttu-id="286bd-146">Kommatall</span><span class="sxs-lookup"><span data-stu-id="286bd-146">Real</span></span>      |          |
  | <span data-ttu-id="286bd-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="286bd-147">HalfDayDefinition</span></span> | <span data-ttu-id="286bd-148">Opplisting</span><span class="sxs-lookup"><span data-stu-id="286bd-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="286bd-149">Handlinger</span><span class="sxs-lookup"><span data-stu-id="286bd-149">Actions</span></span>

 | <span data-ttu-id="286bd-150">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="286bd-150">Action Name</span></span>                               | <span data-ttu-id="286bd-151">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="286bd-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="286bd-152">Send</span><span class="sxs-lookup"><span data-stu-id="286bd-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="286bd-153">Sender forespørselen som skal behandles av en arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="286bd-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="286bd-154">Se også</span><span class="sxs-lookup"><span data-stu-id="286bd-154">See also</span></span>

- [<span data-ttu-id="286bd-155">Sende en permisjonsforespørsel til arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="286bd-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="286bd-156">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="286bd-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]