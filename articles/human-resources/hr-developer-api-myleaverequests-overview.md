---
title: Oversikt over MyLeaveRequests
description: ''
author: andreabichsel
manager: AnnBe
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
ms.openlocfilehash: 66f161d6736b1bb544d02871d9d51b2949b1cfa0
ms.sourcegitcommit: 40163705a134c9874fd33be80c7ae59ccce22c21
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/03/2020
ms.locfileid: "3010067"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="64a25-102">Oversikt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="64a25-102">MyLeaveRequests overview</span></span>

<span data-ttu-id="64a25-103">MyLeaveRequests-enheten i Microsoft Dynamics 365 Human Resources gir listen over permisjonsforespørsler i systemet, begrenset til forespørslene som er tilgjengelige for den gjeldende brukeren som spør enheten.</span><span class="sxs-lookup"><span data-stu-id="64a25-103">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="64a25-104">Nøkkel</span><span class="sxs-lookup"><span data-stu-id="64a25-104">Key</span></span>

  | <span data-ttu-id="64a25-105">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="64a25-105">Property Name</span></span> | <span data-ttu-id="64a25-106">Datatype</span><span class="sxs-lookup"><span data-stu-id="64a25-106">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="64a25-107">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="64a25-107">dataAreaId</span></span>    | <span data-ttu-id="64a25-108">Streng</span><span class="sxs-lookup"><span data-stu-id="64a25-108">String</span></span>    |
  | <span data-ttu-id="64a25-109">RequestId</span><span class="sxs-lookup"><span data-stu-id="64a25-109">RequestId</span></span>     | <span data-ttu-id="64a25-110">Streng</span><span class="sxs-lookup"><span data-stu-id="64a25-110">String</span></span>    |
  | <span data-ttu-id="64a25-111">LeaveType</span><span class="sxs-lookup"><span data-stu-id="64a25-111">LeaveType</span></span>     | <span data-ttu-id="64a25-112">Streng</span><span class="sxs-lookup"><span data-stu-id="64a25-112">String</span></span>    |
  | <span data-ttu-id="64a25-113">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="64a25-113">LeaveDate</span></span>     | <span data-ttu-id="64a25-114">Dato</span><span class="sxs-lookup"><span data-stu-id="64a25-114">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="64a25-115">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="64a25-115">Properties</span></span>

  | <span data-ttu-id="64a25-116">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="64a25-116">Property Name</span></span>     | <span data-ttu-id="64a25-117">Datatype</span><span class="sxs-lookup"><span data-stu-id="64a25-117">Data Type</span></span> | <span data-ttu-id="64a25-118">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="64a25-118">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="64a25-119">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="64a25-119">dataAreaId</span></span>        | <span data-ttu-id="64a25-120">Streng</span><span class="sxs-lookup"><span data-stu-id="64a25-120">String</span></span>    | <span data-ttu-id="64a25-121">X</span><span class="sxs-lookup"><span data-stu-id="64a25-121">X</span></span>        |
  | <span data-ttu-id="64a25-122">RequestId</span><span class="sxs-lookup"><span data-stu-id="64a25-122">RequestId</span></span>         | <span data-ttu-id="64a25-123">Streng</span><span class="sxs-lookup"><span data-stu-id="64a25-123">String</span></span>    | <span data-ttu-id="64a25-124">X</span><span class="sxs-lookup"><span data-stu-id="64a25-124">X</span></span>        |
  | <span data-ttu-id="64a25-125">LeaveType</span><span class="sxs-lookup"><span data-stu-id="64a25-125">LeaveType</span></span>         | <span data-ttu-id="64a25-126">Streng</span><span class="sxs-lookup"><span data-stu-id="64a25-126">String</span></span>    | <span data-ttu-id="64a25-127">X</span><span class="sxs-lookup"><span data-stu-id="64a25-127">X</span></span>        |
  | <span data-ttu-id="64a25-128">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="64a25-128">LeaveDate</span></span>         | <span data-ttu-id="64a25-129">Dato</span><span class="sxs-lookup"><span data-stu-id="64a25-129">Date</span></span>      | <span data-ttu-id="64a25-130">X</span><span class="sxs-lookup"><span data-stu-id="64a25-130">X</span></span>        |
  | <span data-ttu-id="64a25-131">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="64a25-131">ReasonCodeId</span></span>      | <span data-ttu-id="64a25-132">Streng</span><span class="sxs-lookup"><span data-stu-id="64a25-132">String</span></span>    |          |
  | <span data-ttu-id="64a25-133">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="64a25-133">PersonnelNumber</span></span>   | <span data-ttu-id="64a25-134">Streng</span><span class="sxs-lookup"><span data-stu-id="64a25-134">String</span></span>    | <span data-ttu-id="64a25-135">X</span><span class="sxs-lookup"><span data-stu-id="64a25-135">X</span></span>        |
  | <span data-ttu-id="64a25-136">RequestDate</span><span class="sxs-lookup"><span data-stu-id="64a25-136">RequestDate</span></span>       | <span data-ttu-id="64a25-137">Dato</span><span class="sxs-lookup"><span data-stu-id="64a25-137">Date</span></span>      | <span data-ttu-id="64a25-138">X</span><span class="sxs-lookup"><span data-stu-id="64a25-138">X</span></span>        |
  | <span data-ttu-id="64a25-139">Kommentar</span><span class="sxs-lookup"><span data-stu-id="64a25-139">Comment</span></span>           | <span data-ttu-id="64a25-140">Streng</span><span class="sxs-lookup"><span data-stu-id="64a25-140">String</span></span>    |          |
  | <span data-ttu-id="64a25-141">Status</span><span class="sxs-lookup"><span data-stu-id="64a25-141">Status</span></span>            | <span data-ttu-id="64a25-142">Opplisting</span><span class="sxs-lookup"><span data-stu-id="64a25-142">Enum</span></span>      | <span data-ttu-id="64a25-143">X</span><span class="sxs-lookup"><span data-stu-id="64a25-143">X</span></span>        |
  | <span data-ttu-id="64a25-144">Beløp</span><span class="sxs-lookup"><span data-stu-id="64a25-144">Amount</span></span>            | <span data-ttu-id="64a25-145">Kommatall</span><span class="sxs-lookup"><span data-stu-id="64a25-145">Real</span></span>      |          |
  | <span data-ttu-id="64a25-146">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="64a25-146">HalfDayDefinition</span></span> | <span data-ttu-id="64a25-147">Opplisting</span><span class="sxs-lookup"><span data-stu-id="64a25-147">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="64a25-148">Handlinger</span><span class="sxs-lookup"><span data-stu-id="64a25-148">Actions</span></span>

 | <span data-ttu-id="64a25-149">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="64a25-149">Action Name</span></span>                               | <span data-ttu-id="64a25-150">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="64a25-150">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="64a25-151">Send</span><span class="sxs-lookup"><span data-stu-id="64a25-151">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="64a25-152">Sender forespørselen som skal behandles av en arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="64a25-152">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="64a25-153">Se også</span><span class="sxs-lookup"><span data-stu-id="64a25-153">See also</span></span>

- [<span data-ttu-id="64a25-154">Sende en permisjonsforespørsel til arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="64a25-154">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="64a25-155">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="64a25-155">Authentication</span></span>](hr-developer-api-authentication.md)