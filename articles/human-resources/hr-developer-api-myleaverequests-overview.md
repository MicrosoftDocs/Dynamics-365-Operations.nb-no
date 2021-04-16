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
ms.reviewer: anbichse
ms.search.scope: Human Resources
ms.custom: 7521
ms.assetid: ''
ms.search.region: Global
ms.author: anbichse
ms.search.validFrom: 2020-02-03
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 44e23a076733bac782a0366aeba3456911522abe
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5803639"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="e21a2-103">Oversikt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="e21a2-103">MyLeaveRequests overview</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="e21a2-104">MyLeaveRequests-enheten i Microsoft Dynamics 365 Human Resources gir listen over permisjonsforespørsler i systemet, begrenset til forespørslene som er tilgjengelige for den gjeldende brukeren som spør enheten.</span><span class="sxs-lookup"><span data-stu-id="e21a2-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="e21a2-105">Nøkkel</span><span class="sxs-lookup"><span data-stu-id="e21a2-105">Key</span></span>

  | <span data-ttu-id="e21a2-106">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="e21a2-106">Property Name</span></span> | <span data-ttu-id="e21a2-107">Datatype</span><span class="sxs-lookup"><span data-stu-id="e21a2-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="e21a2-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="e21a2-108">dataAreaId</span></span>    | <span data-ttu-id="e21a2-109">Streng</span><span class="sxs-lookup"><span data-stu-id="e21a2-109">String</span></span>    |
  | <span data-ttu-id="e21a2-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="e21a2-110">RequestId</span></span>     | <span data-ttu-id="e21a2-111">Streng</span><span class="sxs-lookup"><span data-stu-id="e21a2-111">String</span></span>    |
  | <span data-ttu-id="e21a2-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="e21a2-112">LeaveType</span></span>     | <span data-ttu-id="e21a2-113">Streng</span><span class="sxs-lookup"><span data-stu-id="e21a2-113">String</span></span>    |
  | <span data-ttu-id="e21a2-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="e21a2-114">LeaveDate</span></span>     | <span data-ttu-id="e21a2-115">Dato</span><span class="sxs-lookup"><span data-stu-id="e21a2-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="e21a2-116">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="e21a2-116">Properties</span></span>

  | <span data-ttu-id="e21a2-117">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="e21a2-117">Property Name</span></span>     | <span data-ttu-id="e21a2-118">Datatype</span><span class="sxs-lookup"><span data-stu-id="e21a2-118">Data Type</span></span> | <span data-ttu-id="e21a2-119">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="e21a2-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="e21a2-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="e21a2-120">dataAreaId</span></span>        | <span data-ttu-id="e21a2-121">Streng</span><span class="sxs-lookup"><span data-stu-id="e21a2-121">String</span></span>    | <span data-ttu-id="e21a2-122">X</span><span class="sxs-lookup"><span data-stu-id="e21a2-122">X</span></span>        |
  | <span data-ttu-id="e21a2-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="e21a2-123">RequestId</span></span>         | <span data-ttu-id="e21a2-124">Streng</span><span class="sxs-lookup"><span data-stu-id="e21a2-124">String</span></span>    | <span data-ttu-id="e21a2-125">X</span><span class="sxs-lookup"><span data-stu-id="e21a2-125">X</span></span>        |
  | <span data-ttu-id="e21a2-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="e21a2-126">LeaveType</span></span>         | <span data-ttu-id="e21a2-127">Streng</span><span class="sxs-lookup"><span data-stu-id="e21a2-127">String</span></span>    | <span data-ttu-id="e21a2-128">X</span><span class="sxs-lookup"><span data-stu-id="e21a2-128">X</span></span>        |
  | <span data-ttu-id="e21a2-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="e21a2-129">LeaveDate</span></span>         | <span data-ttu-id="e21a2-130">Dato</span><span class="sxs-lookup"><span data-stu-id="e21a2-130">Date</span></span>      | <span data-ttu-id="e21a2-131">X</span><span class="sxs-lookup"><span data-stu-id="e21a2-131">X</span></span>        |
  | <span data-ttu-id="e21a2-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="e21a2-132">ReasonCodeId</span></span>      | <span data-ttu-id="e21a2-133">Streng</span><span class="sxs-lookup"><span data-stu-id="e21a2-133">String</span></span>    |          |
  | <span data-ttu-id="e21a2-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="e21a2-134">PersonnelNumber</span></span>   | <span data-ttu-id="e21a2-135">Streng</span><span class="sxs-lookup"><span data-stu-id="e21a2-135">String</span></span>    | <span data-ttu-id="e21a2-136">X</span><span class="sxs-lookup"><span data-stu-id="e21a2-136">X</span></span>        |
  | <span data-ttu-id="e21a2-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="e21a2-137">RequestDate</span></span>       | <span data-ttu-id="e21a2-138">Dato</span><span class="sxs-lookup"><span data-stu-id="e21a2-138">Date</span></span>      | <span data-ttu-id="e21a2-139">X</span><span class="sxs-lookup"><span data-stu-id="e21a2-139">X</span></span>        |
  | <span data-ttu-id="e21a2-140">Kommentar</span><span class="sxs-lookup"><span data-stu-id="e21a2-140">Comment</span></span>           | <span data-ttu-id="e21a2-141">Streng</span><span class="sxs-lookup"><span data-stu-id="e21a2-141">String</span></span>    |          |
  | <span data-ttu-id="e21a2-142">Status</span><span class="sxs-lookup"><span data-stu-id="e21a2-142">Status</span></span>            | <span data-ttu-id="e21a2-143">Opplisting</span><span class="sxs-lookup"><span data-stu-id="e21a2-143">Enum</span></span>      | <span data-ttu-id="e21a2-144">X</span><span class="sxs-lookup"><span data-stu-id="e21a2-144">X</span></span>        |
  | <span data-ttu-id="e21a2-145">Beløp</span><span class="sxs-lookup"><span data-stu-id="e21a2-145">Amount</span></span>            | <span data-ttu-id="e21a2-146">Kommatall</span><span class="sxs-lookup"><span data-stu-id="e21a2-146">Real</span></span>      |          |
  | <span data-ttu-id="e21a2-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="e21a2-147">HalfDayDefinition</span></span> | <span data-ttu-id="e21a2-148">Opplisting</span><span class="sxs-lookup"><span data-stu-id="e21a2-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="e21a2-149">Handlinger</span><span class="sxs-lookup"><span data-stu-id="e21a2-149">Actions</span></span>

 | <span data-ttu-id="e21a2-150">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="e21a2-150">Action Name</span></span>                               | <span data-ttu-id="e21a2-151">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="e21a2-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="e21a2-152">Send</span><span class="sxs-lookup"><span data-stu-id="e21a2-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="e21a2-153">Sender forespørselen som skal behandles av en arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="e21a2-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="e21a2-154">Se også</span><span class="sxs-lookup"><span data-stu-id="e21a2-154">See also</span></span>

- [<span data-ttu-id="e21a2-155">Sende en permisjonsforespørsel til arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="e21a2-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="e21a2-156">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="e21a2-156">Authentication</span></span>](hr-developer-api-authentication.md)

[!INCLUDE[footer-include](../includes/footer-banner.md)]