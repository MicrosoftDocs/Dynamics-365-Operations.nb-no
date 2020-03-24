---
title: Oversikt over MyLeaveRequests
description: MyLeaveRequests-enheten i Microsoft Dynamics 365 Human Resources gir listen over permisjonsforespørsler i systemet, begrenset til forespørslene som er tilgjengelige for den gjeldende brukeren som spør enheten.
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
ms.openlocfilehash: 4bf3b298af9eb39e03514a4005afb43a42908e47
ms.sourcegitcommit: f38302b9430f2ab3efe91d0a7beff946bc610e8f
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/28/2020
ms.locfileid: "3092043"
---
# <a name="myleaverequests-overview"></a><span data-ttu-id="71cd6-103">Oversikt over MyLeaveRequests</span><span class="sxs-lookup"><span data-stu-id="71cd6-103">MyLeaveRequests overview</span></span>

<span data-ttu-id="71cd6-104">MyLeaveRequests-enheten i Microsoft Dynamics 365 Human Resources gir listen over permisjonsforespørsler i systemet, begrenset til forespørslene som er tilgjengelige for den gjeldende brukeren som spør enheten.</span><span class="sxs-lookup"><span data-stu-id="71cd6-104">The MyLeaveRequests entity in Microsoft Dynamics 365 Human Resources provides the list of Leave Requests in the system, scoped (limited) to the requests accessible to the current user querying the entity.</span></span>

## <a name="key"></a><span data-ttu-id="71cd6-105">Nøkkel</span><span class="sxs-lookup"><span data-stu-id="71cd6-105">Key</span></span>

  | <span data-ttu-id="71cd6-106">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="71cd6-106">Property Name</span></span> | <span data-ttu-id="71cd6-107">Datatype</span><span class="sxs-lookup"><span data-stu-id="71cd6-107">Data Type</span></span> |
  |---------------|-----------|
  | <span data-ttu-id="71cd6-108">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="71cd6-108">dataAreaId</span></span>    | <span data-ttu-id="71cd6-109">Streng</span><span class="sxs-lookup"><span data-stu-id="71cd6-109">String</span></span>    |
  | <span data-ttu-id="71cd6-110">RequestId</span><span class="sxs-lookup"><span data-stu-id="71cd6-110">RequestId</span></span>     | <span data-ttu-id="71cd6-111">Streng</span><span class="sxs-lookup"><span data-stu-id="71cd6-111">String</span></span>    |
  | <span data-ttu-id="71cd6-112">LeaveType</span><span class="sxs-lookup"><span data-stu-id="71cd6-112">LeaveType</span></span>     | <span data-ttu-id="71cd6-113">Streng</span><span class="sxs-lookup"><span data-stu-id="71cd6-113">String</span></span>    |
  | <span data-ttu-id="71cd6-114">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="71cd6-114">LeaveDate</span></span>     | <span data-ttu-id="71cd6-115">Dato</span><span class="sxs-lookup"><span data-stu-id="71cd6-115">Date</span></span>      |
  
## <a name="properties"></a><span data-ttu-id="71cd6-116">Egenskaper</span><span class="sxs-lookup"><span data-stu-id="71cd6-116">Properties</span></span>

  | <span data-ttu-id="71cd6-117">Egenskapsnavn</span><span class="sxs-lookup"><span data-stu-id="71cd6-117">Property Name</span></span>     | <span data-ttu-id="71cd6-118">Datatype</span><span class="sxs-lookup"><span data-stu-id="71cd6-118">Data Type</span></span> | <span data-ttu-id="71cd6-119">Obligatorisk</span><span class="sxs-lookup"><span data-stu-id="71cd6-119">Required</span></span> |
  |-------------------|-----------|----------|
  | <span data-ttu-id="71cd6-120">dataAreaId</span><span class="sxs-lookup"><span data-stu-id="71cd6-120">dataAreaId</span></span>        | <span data-ttu-id="71cd6-121">Streng</span><span class="sxs-lookup"><span data-stu-id="71cd6-121">String</span></span>    | <span data-ttu-id="71cd6-122">X</span><span class="sxs-lookup"><span data-stu-id="71cd6-122">X</span></span>        |
  | <span data-ttu-id="71cd6-123">RequestId</span><span class="sxs-lookup"><span data-stu-id="71cd6-123">RequestId</span></span>         | <span data-ttu-id="71cd6-124">Streng</span><span class="sxs-lookup"><span data-stu-id="71cd6-124">String</span></span>    | <span data-ttu-id="71cd6-125">X</span><span class="sxs-lookup"><span data-stu-id="71cd6-125">X</span></span>        |
  | <span data-ttu-id="71cd6-126">LeaveType</span><span class="sxs-lookup"><span data-stu-id="71cd6-126">LeaveType</span></span>         | <span data-ttu-id="71cd6-127">Streng</span><span class="sxs-lookup"><span data-stu-id="71cd6-127">String</span></span>    | <span data-ttu-id="71cd6-128">X</span><span class="sxs-lookup"><span data-stu-id="71cd6-128">X</span></span>        |
  | <span data-ttu-id="71cd6-129">LeaveDate</span><span class="sxs-lookup"><span data-stu-id="71cd6-129">LeaveDate</span></span>         | <span data-ttu-id="71cd6-130">Dato</span><span class="sxs-lookup"><span data-stu-id="71cd6-130">Date</span></span>      | <span data-ttu-id="71cd6-131">X</span><span class="sxs-lookup"><span data-stu-id="71cd6-131">X</span></span>        |
  | <span data-ttu-id="71cd6-132">ReasonCodeId</span><span class="sxs-lookup"><span data-stu-id="71cd6-132">ReasonCodeId</span></span>      | <span data-ttu-id="71cd6-133">Streng</span><span class="sxs-lookup"><span data-stu-id="71cd6-133">String</span></span>    |          |
  | <span data-ttu-id="71cd6-134">PersonnelNumber</span><span class="sxs-lookup"><span data-stu-id="71cd6-134">PersonnelNumber</span></span>   | <span data-ttu-id="71cd6-135">Streng</span><span class="sxs-lookup"><span data-stu-id="71cd6-135">String</span></span>    | <span data-ttu-id="71cd6-136">X</span><span class="sxs-lookup"><span data-stu-id="71cd6-136">X</span></span>        |
  | <span data-ttu-id="71cd6-137">RequestDate</span><span class="sxs-lookup"><span data-stu-id="71cd6-137">RequestDate</span></span>       | <span data-ttu-id="71cd6-138">Dato</span><span class="sxs-lookup"><span data-stu-id="71cd6-138">Date</span></span>      | <span data-ttu-id="71cd6-139">X</span><span class="sxs-lookup"><span data-stu-id="71cd6-139">X</span></span>        |
  | <span data-ttu-id="71cd6-140">Kommentar</span><span class="sxs-lookup"><span data-stu-id="71cd6-140">Comment</span></span>           | <span data-ttu-id="71cd6-141">Streng</span><span class="sxs-lookup"><span data-stu-id="71cd6-141">String</span></span>    |          |
  | <span data-ttu-id="71cd6-142">Status</span><span class="sxs-lookup"><span data-stu-id="71cd6-142">Status</span></span>            | <span data-ttu-id="71cd6-143">Opplisting</span><span class="sxs-lookup"><span data-stu-id="71cd6-143">Enum</span></span>      | <span data-ttu-id="71cd6-144">X</span><span class="sxs-lookup"><span data-stu-id="71cd6-144">X</span></span>        |
  | <span data-ttu-id="71cd6-145">Beløp</span><span class="sxs-lookup"><span data-stu-id="71cd6-145">Amount</span></span>            | <span data-ttu-id="71cd6-146">Kommatall</span><span class="sxs-lookup"><span data-stu-id="71cd6-146">Real</span></span>      |          |
  | <span data-ttu-id="71cd6-147">HalfDayDefinition</span><span class="sxs-lookup"><span data-stu-id="71cd6-147">HalfDayDefinition</span></span> | <span data-ttu-id="71cd6-148">Opplisting</span><span class="sxs-lookup"><span data-stu-id="71cd6-148">Enum</span></span>      |          |

## <a name="actions"></a><span data-ttu-id="71cd6-149">Handlinger</span><span class="sxs-lookup"><span data-stu-id="71cd6-149">Actions</span></span>

 | <span data-ttu-id="71cd6-150">Handlingsnavn</span><span class="sxs-lookup"><span data-stu-id="71cd6-150">Action Name</span></span>                               | <span data-ttu-id="71cd6-151">Beskrivelse</span><span class="sxs-lookup"><span data-stu-id="71cd6-151">Description</span></span>                                     |
 |-------------------------------------------|-------------------------------------------------|
 | [<span data-ttu-id="71cd6-152">Send</span><span class="sxs-lookup"><span data-stu-id="71cd6-152">submit</span></span>](hr-developer-api-myleaverequests-submit.md)   | <span data-ttu-id="71cd6-153">Sender forespørselen som skal behandles av en arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="71cd6-153">Submit the request to be processed by workflow.</span></span> |

## <a name="see-also"></a><span data-ttu-id="71cd6-154">Se også</span><span class="sxs-lookup"><span data-stu-id="71cd6-154">See also</span></span>

- [<span data-ttu-id="71cd6-155">Sende en permisjonsforespørsel til arbeidsflyt</span><span class="sxs-lookup"><span data-stu-id="71cd6-155">Submit a leave request to workflow</span></span>](hr-developer-api-myleaverequests-submit.md)
- [<span data-ttu-id="71cd6-156">Godkjenning</span><span class="sxs-lookup"><span data-stu-id="71cd6-156">Authentication</span></span>](hr-developer-api-authentication.md)