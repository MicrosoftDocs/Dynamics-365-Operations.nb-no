---
title: Oversikt over MyLeaveRequests
description: MyLeaveRequests-enheten i Microsoft Dynamics 365 Human Resources gir listen over permisjonsforespørsler i systemet, begrenset til forespørslene som er tilgjengelige for den gjeldende brukeren som spør enheten.
author: andreabichsel
ms.date: 02/03/2020
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: ''
audience: Application User
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: f29d5cf1469b58b4ea1837dc82b9513f5c002609
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6054962"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="33798-103">Oversikt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="33798-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="33798-104">MyLeaveRequests-enheten i Microsoft Dynamics 365 Human Resources gir listen over permisjonsforespørsler i systemet, begrenset til forespørslene som er tilgjengelige for den gjeldende brukeren som spør enheten.</span><span class="sxs-lookup"><span data-stu-id="33798-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="33798-105">Nøkkel</span><span class="sxs-lookup"><span data-stu-id="33798-105">Key</span></span>

  | <span data-ttu-id="33798-106">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="33798-106">Property Name</span></span> | <span data-ttu-id="33798-107">Datatype</span><span class="sxs-lookup"><span data-stu-id="33798-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="33798-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="33798-108">dataAreaId</span></span>    | <span data-ttu-id="33798-109">Streng</span><span class="sxs-lookup"><span data-stu-id="33798-109">String</span></span>    |
  | <span data-ttu-id="33798-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="33798-110">RequestId</span></span>     | <span data-ttu-id="33798-111">Streng</span><span class="sxs-lookup"><span data-stu-id="33798-111">String</span></span>    |
  | <span data-ttu-id="33798-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="33798-112">LeaveType</span></span>     | <span data-ttu-id="33798-113">Streng</span><span class="sxs-lookup"><span data-stu-id="33798-113">String</span></span>    |
  | <span data-ttu-id="33798-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="33798-114">LeaveDate</span></span>     | <span data-ttu-id="33798-115">Dato</span><span class="sxs-lookup"><span data-stu-id="33798-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="33798-116">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="33798-116">Properties</span></span>

  | <span data-ttu-id="33798-117">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="33798-117">Property Name</span></span>     | <span data-ttu-id="33798-118">Datatype</span><span class="sxs-lookup"><span data-stu-id="33798-118">Data Type</span></span> | <span data-ttu-id="33798-119">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="33798-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="33798-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="33798-120">dataAreaId</span></span>        | <span data-ttu-id="33798-121">Streng</span><span class="sxs-lookup"><span data-stu-id="33798-121">String</span></span>    | <span data-ttu-id="33798-122">X</span><span class="sxs-lookup"><span data-stu-id="33798-122">X</span></span>        |
  | <span data-ttu-id="33798-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="33798-123">RequestId</span></span>         | <span data-ttu-id="33798-124">Streng</span><span class="sxs-lookup"><span data-stu-id="33798-124">String</span></span>    | <span data-ttu-id="33798-125">X</span><span class="sxs-lookup"><span data-stu-id="33798-125">X</span></span>        |
  | <span data-ttu-id="33798-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="33798-126">LeaveType</span></span>         | <span data-ttu-id="33798-127">Streng</span><span class="sxs-lookup"><span data-stu-id="33798-127">String</span></span>    | <span data-ttu-id="33798-128">X</span><span class="sxs-lookup"><span data-stu-id="33798-128">X</span></span>        |
  | <span data-ttu-id="33798-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="33798-129">LeaveDate</span></span>         | <span data-ttu-id="33798-130">Dato</span><span class="sxs-lookup"><span data-stu-id="33798-130">Date</span></span>      | <span data-ttu-id="33798-131">X</span><span class="sxs-lookup"><span data-stu-id="33798-131">X</span></span>        |
  | <span data-ttu-id="33798-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="33798-132">ReasonCodeId</span></span>      | <span data-ttu-id="33798-133">Streng</span><span class="sxs-lookup"><span data-stu-id="33798-133">String</span></span>    |          |
  | <span data-ttu-id="33798-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="33798-134">PersonnelNumber</span></span>   | <span data-ttu-id="33798-135">Streng</span><span class="sxs-lookup"><span data-stu-id="33798-135">String</span></span>    | <span data-ttu-id="33798-136">X</span><span class="sxs-lookup"><span data-stu-id="33798-136">X</span></span>        |
  | <span data-ttu-id="33798-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="33798-137">RequestDate</span></span>       | <span data-ttu-id="33798-138">Dato</span><span class="sxs-lookup"><span data-stu-id="33798-138">Date</span></span>      | <span data-ttu-id="33798-139">X</span><span class="sxs-lookup"><span data-stu-id="33798-139">X</span></span>        |
  | <span data-ttu-id="33798-140">Kommentar</span><span class="sxs-lookup"><span data-stu-id="33798-140">Comment</span></span>           | <span data-ttu-id="33798-141">Streng</span><span class="sxs-lookup"><span data-stu-id="33798-141">String</span></span>    |          |
  | <span data-ttu-id="33798-142">Status</span><span class="sxs-lookup"><span data-stu-id="33798-142">Status</span></span>            | <span data-ttu-id="33798-143">Opplisting</span><span class="sxs-lookup"><span data-stu-id="33798-143">Enum</span></span>      | <span data-ttu-id="33798-144">X</span><span class="sxs-lookup"><span data-stu-id="33798-144">X</span></span>        |
  | <span data-ttu-id="33798-145">Beløp</span><span class="sxs-lookup"><span data-stu-id="33798-145">Amount</span></span>            | <span data-ttu-id="33798-146">Kommatall</span><span class="sxs-lookup"><span data-stu-id="33798-146">Real</span></span>      |          |
  | <span data-ttu-id="33798-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="33798-147">HalfDayDefinition</span></span> | <span data-ttu-id="33798-148">Opplisting</span><span class="sxs-lookup"><span data-stu-id="33798-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="33798-149">Handlinger</span><span class="sxs-lookup"><span data-stu-id="33798-149">Actions</span></span>

 | <span data-ttu-id="33798-150">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="33798-150">Action Name</span></span>                               | <span data-ttu-id="33798-151">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="33798-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="33798-152">Send</span><span class="sxs-lookup"><span data-stu-id="33798-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="33798-153">Sender forespørselen som skal behandles av en arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="33798-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="33798-154">Se også</span><span class="sxs-lookup"><span data-stu-id="33798-154">See also</span></span>

- [<span data-ttu-id="33798-155">Sende en permisjonsforespørsel til arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="33798-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="33798-156">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="33798-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]