---
title: Rekrutteringsforespørselsstatus
description: Dette emnet beskriver alternativsettet for Rekrutteringsforespørselsstatus for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 0032e6bfdbfd2792dafda8bf24a1b0cbc551740d
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464652"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="59461-103">Rekrutteringsforespørselsstatus</span><span class="sxs-lookup"><span data-stu-id="59461-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="59461-104">Dette emnet beskriver alternativsettet for Rekrutteringsforespørselsstatus for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="59461-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="59461-105">Fysisk navn: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="59461-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="59461-106">Denne opplistingen gir alternativsettet for statusverdiene for en RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="59461-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="59461-107">Verdi</span><span class="sxs-lookup"><span data-stu-id="59461-107">Value</span></span> | <span data-ttu-id="59461-108">Etikett</span><span class="sxs-lookup"><span data-stu-id="59461-108">Label</span></span> | <span data-ttu-id="59461-109">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="59461-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="59461-110">200000000</span><span class="sxs-lookup"><span data-stu-id="59461-110">200000000</span></span> | <span data-ttu-id="59461-111">Utkast</span><span class="sxs-lookup"><span data-stu-id="59461-111">Draft</span></span> | <span data-ttu-id="59461-112">Forespørselen er i utkast og er ikke klar for aktiv rekruttering.</span><span class="sxs-lookup"><span data-stu-id="59461-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="59461-113">200000001</span><span class="sxs-lookup"><span data-stu-id="59461-113">200000001</span></span> | <span data-ttu-id="59461-114">Til gjennomgang</span><span class="sxs-lookup"><span data-stu-id="59461-114">In Review</span></span> | <span data-ttu-id="59461-115">Forespørselen er sendt og rutes til godkjenning etter arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="59461-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="59461-116">Bare tilgjengelig når arbeidsflyten er aktivert.</span><span class="sxs-lookup"><span data-stu-id="59461-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="59461-117">200000002</span><span class="sxs-lookup"><span data-stu-id="59461-117">200000002</span></span> | <span data-ttu-id="59461-118">Uavsluttet</span><span class="sxs-lookup"><span data-stu-id="59461-118">Pending</span></span> | <span data-ttu-id="59461-119">Forespørselen venter på arbeidsflythandling.</span><span class="sxs-lookup"><span data-stu-id="59461-119">The request is pending workflow action.</span></span> <span data-ttu-id="59461-120">Bare tilgjengelig når arbeidsflyten er aktivert.</span><span class="sxs-lookup"><span data-stu-id="59461-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="59461-121">200000003</span><span class="sxs-lookup"><span data-stu-id="59461-121">200000003</span></span> | <span data-ttu-id="59461-122">Annullert</span><span class="sxs-lookup"><span data-stu-id="59461-122">Canceled</span></span> | <span data-ttu-id="59461-123">Forespørselen har blitt avbrutt.</span><span class="sxs-lookup"><span data-stu-id="59461-123">The request has been canceled.</span></span> <span data-ttu-id="59461-124">Bare tilgjengelig når arbeidsflyten er aktivert.</span><span class="sxs-lookup"><span data-stu-id="59461-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="59461-125">200000004</span><span class="sxs-lookup"><span data-stu-id="59461-125">200000004</span></span> | <span data-ttu-id="59461-126">Nektet</span><span class="sxs-lookup"><span data-stu-id="59461-126">Denied</span></span> | <span data-ttu-id="59461-127">Forespørselen er avvist.</span><span class="sxs-lookup"><span data-stu-id="59461-127">The request has been denied.</span></span> <span data-ttu-id="59461-128">Bare tilgjengelig når arbeidsflyten er aktivert.</span><span class="sxs-lookup"><span data-stu-id="59461-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="59461-129">200000005</span><span class="sxs-lookup"><span data-stu-id="59461-129">200000005</span></span> | <span data-ttu-id="59461-130">Aktive</span><span class="sxs-lookup"><span data-stu-id="59461-130">Active</span></span> | <span data-ttu-id="59461-131">Alle arbeidsflyter fullføres og godkjennes, og forespørselen er klar for aktiv rekruttering.</span><span class="sxs-lookup"><span data-stu-id="59461-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="59461-132">200000006</span><span class="sxs-lookup"><span data-stu-id="59461-132">200000006</span></span> | <span data-ttu-id="59461-133">Forseglet</span><span class="sxs-lookup"><span data-stu-id="59461-133">Closed</span></span> | <span data-ttu-id="59461-134">Rekrutteringsforespørselen er lukket.</span><span class="sxs-lookup"><span data-stu-id="59461-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="59461-135">Se også</span><span class="sxs-lookup"><span data-stu-id="59461-135">See also</span></span>

[<span data-ttu-id="59461-136">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="59461-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="59461-137">Eksempelspørring for rekrutteringsforespørsel</span><span class="sxs-lookup"><span data-stu-id="59461-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]