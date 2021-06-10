---
title: Rekrutteringsforespørselsstatus
description: Dette emnet beskriver alternativsettet for Rekrutteringsforespørselsstatus for Dynamics 365 Human Resources.
author: jaredha
ms.date: 02/05/2021
ms.topic: article
ms.prod: ''
ms.technology: ''
audience: Application User
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.author: jaredha
ms.search.validFrom: 2021-02-05
ms.dyn365.ops.version: Human Resources
ms.openlocfilehash: 3b05cc531a84144708ff52913927bbd04574a3b2
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6059190"
---
# <a name="recruiting-request-status"></a><span data-ttu-id="877eb-103">Rekrutteringsforespørselsstatus</span><span class="sxs-lookup"><span data-stu-id="877eb-103">Recruiting request status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="877eb-104">Dette emnet beskriver alternativsettet for Rekrutteringsforespørselsstatus for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="877eb-104">This topic describes the Recruiting request status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="877eb-105">Fysisk navn: mshr_hcmrecruitingrequeststatus</span><span class="sxs-lookup"><span data-stu-id="877eb-105">Physical name: mshr_hcmrecruitingrequeststatus</span></span>

<span data-ttu-id="877eb-106">Denne opplistingen gir alternativsettet for statusverdiene for en RecruitingRequest.</span><span class="sxs-lookup"><span data-stu-id="877eb-106">This enumeration provides the option set for the status values of a RecruitingRequest.</span></span>

| <span data-ttu-id="877eb-107">Verdi</span><span class="sxs-lookup"><span data-stu-id="877eb-107">Value</span></span> | <span data-ttu-id="877eb-108">Etikett</span><span class="sxs-lookup"><span data-stu-id="877eb-108">Label</span></span> | <span data-ttu-id="877eb-109">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="877eb-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="877eb-110">200000000</span><span class="sxs-lookup"><span data-stu-id="877eb-110">200000000</span></span> | <span data-ttu-id="877eb-111">Utkast</span><span class="sxs-lookup"><span data-stu-id="877eb-111">Draft</span></span> | <span data-ttu-id="877eb-112">Forespørselen er i utkast og er ikke klar for aktiv rekruttering.</span><span class="sxs-lookup"><span data-stu-id="877eb-112">The request is in draft and isn't ready for active recruiting.</span></span> |
| <span data-ttu-id="877eb-113">200000001</span><span class="sxs-lookup"><span data-stu-id="877eb-113">200000001</span></span> | <span data-ttu-id="877eb-114">Til gjennomgang</span><span class="sxs-lookup"><span data-stu-id="877eb-114">In Review</span></span> | <span data-ttu-id="877eb-115">Forespørselen er sendt og rutes til godkjenning etter arbeidsflyt.</span><span class="sxs-lookup"><span data-stu-id="877eb-115">The request has been submitted and is being routed for approval by workflow.</span></span> <span data-ttu-id="877eb-116">Bare tilgjengelig når arbeidsflyten er aktivert.</span><span class="sxs-lookup"><span data-stu-id="877eb-116">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="877eb-117">200000002</span><span class="sxs-lookup"><span data-stu-id="877eb-117">200000002</span></span> | <span data-ttu-id="877eb-118">Uavsluttet</span><span class="sxs-lookup"><span data-stu-id="877eb-118">Pending</span></span> | <span data-ttu-id="877eb-119">Forespørselen venter på arbeidsflythandling.</span><span class="sxs-lookup"><span data-stu-id="877eb-119">The request is pending workflow action.</span></span> <span data-ttu-id="877eb-120">Bare tilgjengelig når arbeidsflyten er aktivert.</span><span class="sxs-lookup"><span data-stu-id="877eb-120">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="877eb-121">200000003</span><span class="sxs-lookup"><span data-stu-id="877eb-121">200000003</span></span> | <span data-ttu-id="877eb-122">Annullert</span><span class="sxs-lookup"><span data-stu-id="877eb-122">Canceled</span></span> | <span data-ttu-id="877eb-123">Forespørselen har blitt avbrutt.</span><span class="sxs-lookup"><span data-stu-id="877eb-123">The request has been canceled.</span></span> <span data-ttu-id="877eb-124">Bare tilgjengelig når arbeidsflyten er aktivert.</span><span class="sxs-lookup"><span data-stu-id="877eb-124">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="877eb-125">200000004</span><span class="sxs-lookup"><span data-stu-id="877eb-125">200000004</span></span> | <span data-ttu-id="877eb-126">Nektet</span><span class="sxs-lookup"><span data-stu-id="877eb-126">Denied</span></span> | <span data-ttu-id="877eb-127">Forespørselen er avvist.</span><span class="sxs-lookup"><span data-stu-id="877eb-127">The request has been denied.</span></span> <span data-ttu-id="877eb-128">Bare tilgjengelig når arbeidsflyten er aktivert.</span><span class="sxs-lookup"><span data-stu-id="877eb-128">Only available when workflow is enabled.</span></span> |
| <span data-ttu-id="877eb-129">200000005</span><span class="sxs-lookup"><span data-stu-id="877eb-129">200000005</span></span> | <span data-ttu-id="877eb-130">Aktive</span><span class="sxs-lookup"><span data-stu-id="877eb-130">Active</span></span> | <span data-ttu-id="877eb-131">Alle arbeidsflyter fullføres og godkjennes, og forespørselen er klar for aktiv rekruttering.</span><span class="sxs-lookup"><span data-stu-id="877eb-131">Any workflow is completed and approved, and the request is ready for active recruiting.</span></span> |
| <span data-ttu-id="877eb-132">200000006</span><span class="sxs-lookup"><span data-stu-id="877eb-132">200000006</span></span> | <span data-ttu-id="877eb-133">Forseglet</span><span class="sxs-lookup"><span data-stu-id="877eb-133">Closed</span></span> | <span data-ttu-id="877eb-134">Rekrutteringsforespørselen er lukket.</span><span class="sxs-lookup"><span data-stu-id="877eb-134">The recruiting request is closed.</span></span> |

## <a name="see-also"></a><span data-ttu-id="877eb-135">Se også</span><span class="sxs-lookup"><span data-stu-id="877eb-135">See also</span></span>

[<span data-ttu-id="877eb-136">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="877eb-136">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="877eb-137">Eksempelspørring for rekrutteringsforespørsel</span><span class="sxs-lookup"><span data-stu-id="877eb-137">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]