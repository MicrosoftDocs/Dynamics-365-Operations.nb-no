---
title: Rekrutteringsforespørselsstatus
description: Dette emnet beskriver alternativsettet for Rekrutteringsforespørselsstatus for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 888fbc511bffbecd837c929049006266191da5ba
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5806048"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="cc0d3-103">Rekrutteringsforespørselsstatus</span><span class="sxs-lookup"><span data-stu-id="cc0d3-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="cc0d3-104">Dette emnet beskriver alternativsettet for Rekrutteringsforespørselsstatus for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="cc0d3-105">Fysisk navn: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="cc0d3-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="cc0d3-106">Denne opplistingen gir alternativsettet for statusverdiene for en RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="cc0d3-107">Verdi</span><span class="sxs-lookup"><span data-stu-id="cc0d3-107">Value</span></span> | <span data-ttu-id="cc0d3-108">Etikett</span><span class="sxs-lookup"><span data-stu-id="cc0d3-108">Label</span></span> | <span data-ttu-id="cc0d3-109">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="cc0d3-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="cc0d3-110">200000000</span><span class="sxs-lookup"><span data-stu-id="cc0d3-110">200000000</span></span> | <span data-ttu-id="cc0d3-111">Utkast</span><span class="sxs-lookup"><span data-stu-id="cc0d3-111">Draft</span></span> | <span data-ttu-id="cc0d3-112">Forespørselen er i utkast og er ikke klar for aktiv rekruttering.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="cc0d3-113">200000001</span><span class="sxs-lookup"><span data-stu-id="cc0d3-113">200000001</span></span> | <span data-ttu-id="cc0d3-114">Til gjennomgang</span><span class="sxs-lookup"><span data-stu-id="cc0d3-114">In Review</span></span> | <span data-ttu-id="cc0d3-115">Forespørselen er sendt og rutes til godkjenning etter arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="cc0d3-116">Bare tilgjengelig når arbeidsflyten er aktivert.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="cc0d3-117">200000002</span><span class="sxs-lookup"><span data-stu-id="cc0d3-117">200000002</span></span> | <span data-ttu-id="cc0d3-118">Uavsluttet</span><span class="sxs-lookup"><span data-stu-id="cc0d3-118">Pending</span></span> | <span data-ttu-id="cc0d3-119">Forespørselen venter på arbeidsflythandling.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-119">The request is pending workflow action.</span></span> <span data-ttu-id="cc0d3-120">Bare tilgjengelig når arbeidsflyten er aktivert.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="cc0d3-121">200000003</span><span class="sxs-lookup"><span data-stu-id="cc0d3-121">200000003</span></span> | <span data-ttu-id="cc0d3-122">Annullert</span><span class="sxs-lookup"><span data-stu-id="cc0d3-122">Canceled</span></span> | <span data-ttu-id="cc0d3-123">Forespørselen har blitt avbrutt.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-123">The request has been canceled.</span></span> <span data-ttu-id="cc0d3-124">Bare tilgjengelig når arbeidsflyten er aktivert.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="cc0d3-125">200000004</span><span class="sxs-lookup"><span data-stu-id="cc0d3-125">200000004</span></span> | <span data-ttu-id="cc0d3-126">Nektet</span><span class="sxs-lookup"><span data-stu-id="cc0d3-126">Denied</span></span> | <span data-ttu-id="cc0d3-127">Forespørselen er avvist.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-127">The request has been denied.</span></span> <span data-ttu-id="cc0d3-128">Bare tilgjengelig når arbeidsflyten er aktivert.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="cc0d3-129">200000005</span><span class="sxs-lookup"><span data-stu-id="cc0d3-129">200000005</span></span> | <span data-ttu-id="cc0d3-130">Aktive</span><span class="sxs-lookup"><span data-stu-id="cc0d3-130">Active</span></span> | <span data-ttu-id="cc0d3-131">Alle arbeidsflyter fullføres og godkjennes, og forespørselen er klar for aktiv rekruttering.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="cc0d3-132">200000006</span><span class="sxs-lookup"><span data-stu-id="cc0d3-132">200000006</span></span> | <span data-ttu-id="cc0d3-133">Forseglet</span><span class="sxs-lookup"><span data-stu-id="cc0d3-133">Closed</span></span> | <span data-ttu-id="cc0d3-134">Rekrutteringsforespørselen er lukket.</span><span class="sxs-lookup"><span data-stu-id="cc0d3-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="cc0d3-135">Se også</span><span class="sxs-lookup"><span data-stu-id="cc0d3-135">See also</span></span>

[<span data-ttu-id="cc0d3-136">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="cc0d3-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="cc0d3-137">Eksempelspørring for rekrutteringsforespørsel</span><span class="sxs-lookup"><span data-stu-id="cc0d3-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]