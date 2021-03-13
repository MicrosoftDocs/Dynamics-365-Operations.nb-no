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
ms.openlocfilehash: 0ca5bc225400338e76faee41a279e91fc00ce570
ms.sourcegitcommit: 18e626c49ccfdb12c1484b985e3a275e51f61320
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/04/2021
ms.locfileid: "5115542"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="d2230-103">Oversikt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="d2230-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="d2230-104">MyLeaveRequests-enheten i Microsoft Dynamics 365 Human Resources gir listen over permisjonsforespørsler i systemet, begrenset til forespørslene som er tilgjengelige for den gjeldende brukeren som spør enheten.</span><span class="sxs-lookup"><span data-stu-id="d2230-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="d2230-105">Nøkkel</span><span class="sxs-lookup"><span data-stu-id="d2230-105">Key</span></span>

  | <span data-ttu-id="d2230-106">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="d2230-106">Property Name</span></span> | <span data-ttu-id="d2230-107">Datatype</span><span class="sxs-lookup"><span data-stu-id="d2230-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="d2230-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="d2230-108">dataAreaId</span></span>    | <span data-ttu-id="d2230-109">Streng</span><span class="sxs-lookup"><span data-stu-id="d2230-109">String</span></span>    |
  | <span data-ttu-id="d2230-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="d2230-110">RequestId</span></span>     | <span data-ttu-id="d2230-111">Streng</span><span class="sxs-lookup"><span data-stu-id="d2230-111">String</span></span>    |
  | <span data-ttu-id="d2230-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="d2230-112">LeaveType</span></span>     | <span data-ttu-id="d2230-113">Streng</span><span class="sxs-lookup"><span data-stu-id="d2230-113">String</span></span>    |
  | <span data-ttu-id="d2230-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="d2230-114">LeaveDate</span></span>     | <span data-ttu-id="d2230-115">Dato</span><span class="sxs-lookup"><span data-stu-id="d2230-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="d2230-116">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="d2230-116">Properties</span></span>

  | <span data-ttu-id="d2230-117">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="d2230-117">Property Name</span></span>     | <span data-ttu-id="d2230-118">Datatype</span><span class="sxs-lookup"><span data-stu-id="d2230-118">Data Type</span></span> | <span data-ttu-id="d2230-119">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="d2230-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="d2230-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="d2230-120">dataAreaId</span></span>        | <span data-ttu-id="d2230-121">Streng</span><span class="sxs-lookup"><span data-stu-id="d2230-121">String</span></span>    | <span data-ttu-id="d2230-122">X</span><span class="sxs-lookup"><span data-stu-id="d2230-122">X</span></span>        |
  | <span data-ttu-id="d2230-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="d2230-123">RequestId</span></span>         | <span data-ttu-id="d2230-124">Streng</span><span class="sxs-lookup"><span data-stu-id="d2230-124">String</span></span>    | <span data-ttu-id="d2230-125">X</span><span class="sxs-lookup"><span data-stu-id="d2230-125">X</span></span>        |
  | <span data-ttu-id="d2230-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="d2230-126">LeaveType</span></span>         | <span data-ttu-id="d2230-127">Streng</span><span class="sxs-lookup"><span data-stu-id="d2230-127">String</span></span>    | <span data-ttu-id="d2230-128">X</span><span class="sxs-lookup"><span data-stu-id="d2230-128">X</span></span>        |
  | <span data-ttu-id="d2230-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="d2230-129">LeaveDate</span></span>         | <span data-ttu-id="d2230-130">Dato</span><span class="sxs-lookup"><span data-stu-id="d2230-130">Date</span></span>      | <span data-ttu-id="d2230-131">X</span><span class="sxs-lookup"><span data-stu-id="d2230-131">X</span></span>        |
  | <span data-ttu-id="d2230-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="d2230-132">ReasonCodeId</span></span>      | <span data-ttu-id="d2230-133">Streng</span><span class="sxs-lookup"><span data-stu-id="d2230-133">String</span></span>    |          |
  | <span data-ttu-id="d2230-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="d2230-134">PersonnelNumber</span></span>   | <span data-ttu-id="d2230-135">Streng</span><span class="sxs-lookup"><span data-stu-id="d2230-135">String</span></span>    | <span data-ttu-id="d2230-136">X</span><span class="sxs-lookup"><span data-stu-id="d2230-136">X</span></span>        |
  | <span data-ttu-id="d2230-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="d2230-137">RequestDate</span></span>       | <span data-ttu-id="d2230-138">Dato</span><span class="sxs-lookup"><span data-stu-id="d2230-138">Date</span></span>      | <span data-ttu-id="d2230-139">X</span><span class="sxs-lookup"><span data-stu-id="d2230-139">X</span></span>        |
  | <span data-ttu-id="d2230-140">Kommentar</span><span class="sxs-lookup"><span data-stu-id="d2230-140">Comment</span></span>           | <span data-ttu-id="d2230-141">Streng</span><span class="sxs-lookup"><span data-stu-id="d2230-141">String</span></span>    |          |
  | <span data-ttu-id="d2230-142">Status</span><span class="sxs-lookup"><span data-stu-id="d2230-142">Status</span></span>            | <span data-ttu-id="d2230-143">Opplisting</span><span class="sxs-lookup"><span data-stu-id="d2230-143">Enum</span></span>      | <span data-ttu-id="d2230-144">X</span><span class="sxs-lookup"><span data-stu-id="d2230-144">X</span></span>        |
  | <span data-ttu-id="d2230-145">Beløp</span><span class="sxs-lookup"><span data-stu-id="d2230-145">Amount</span></span>            | <span data-ttu-id="d2230-146">Kommatall</span><span class="sxs-lookup"><span data-stu-id="d2230-146">Real</span></span>      |          |
  | <span data-ttu-id="d2230-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="d2230-147">HalfDayDefinition</span></span> | <span data-ttu-id="d2230-148">Opplisting</span><span class="sxs-lookup"><span data-stu-id="d2230-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="d2230-149">Handlinger</span><span class="sxs-lookup"><span data-stu-id="d2230-149">Actions</span></span>

 | <span data-ttu-id="d2230-150">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="d2230-150">Action Name</span></span>                               | <span data-ttu-id="d2230-151">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="d2230-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="d2230-152">Send</span><span class="sxs-lookup"><span data-stu-id="d2230-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="d2230-153">Sender forespørselen som skal behandles av en arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="d2230-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="d2230-154">Se også</span><span class="sxs-lookup"><span data-stu-id="d2230-154">See also</span></span>

- [<span data-ttu-id="d2230-155">Sende en permisjonsforespørsel til arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="d2230-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="d2230-156">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="d2230-156">Authentication</span></span>](hr-developer-api-authentication.md)