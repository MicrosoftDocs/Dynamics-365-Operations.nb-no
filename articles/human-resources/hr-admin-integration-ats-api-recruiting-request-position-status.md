---
title: Status for rekrutteringsforespørselsstilling
description: Dette emnet beskriver status for stillingen i en rekrutteringsforespørsel for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 3f7bae64f58f0bdc1603b3c1b5493f1ebcfa8de9
ms.sourcegitcommit: 33b5c8bc4f9461e290513aa22de1ec1fba3b0742
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/05/2021
ms.locfileid: "5126056"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="a93c6-103">Status for rekrutteringsforespørselsstilling</span><span class="sxs-lookup"><span data-stu-id="a93c6-103">Recruiting request position status</span></span>

<span data-ttu-id="a93c6-104">Dette emnet beskriver status for stillingen i en rekrutteringsforespørsel for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a93c6-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="a93c6-105">Fysisk navn: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="a93c6-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="a93c6-106">Denne opplistingen gir alternativetsett for statusverdiene til hver stilling en rekrutteringsforespørsel i RecruitingRequestPosition-enheten.</span><span class="sxs-lookup"><span data-stu-id="a93c6-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="a93c6-107">Verdi</span><span class="sxs-lookup"><span data-stu-id="a93c6-107">Value</span></span> | <span data-ttu-id="a93c6-108">Etikett</span><span class="sxs-lookup"><span data-stu-id="a93c6-108">Label</span></span> | <span data-ttu-id="a93c6-109">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a93c6-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a93c6-110">200000000</span><span class="sxs-lookup"><span data-stu-id="a93c6-110">200000000</span></span> | <span data-ttu-id="a93c6-111">Åpen</span><span class="sxs-lookup"><span data-stu-id="a93c6-111">Open</span></span> | <span data-ttu-id="a93c6-112">Stillingen i rekrutteringsforespørselen er åpen for rekruttering.</span><span class="sxs-lookup"><span data-stu-id="a93c6-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="a93c6-113">Dette viser ikke at det for øyeblikket ikke er noen aktiv stillingstilordning for stillingen.</span><span class="sxs-lookup"><span data-stu-id="a93c6-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="a93c6-114">Det kan være en ansatt i stillingen når rekrutteringen gjøres.</span><span class="sxs-lookup"><span data-stu-id="a93c6-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="a93c6-115">Den viser bare at stillingen er tilgjengelig for rekruttering i konteksten med rekrutteringsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="a93c6-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="a93c6-116">200000001</span><span class="sxs-lookup"><span data-stu-id="a93c6-116">200000001</span></span> | <span data-ttu-id="a93c6-117">Besatt</span><span class="sxs-lookup"><span data-stu-id="a93c6-117">Filled</span></span> | <span data-ttu-id="a93c6-118">En arbeider er valgt for tilordning til stillingen.</span><span class="sxs-lookup"><span data-stu-id="a93c6-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="a93c6-119">200000002</span><span class="sxs-lookup"><span data-stu-id="a93c6-119">200000002</span></span> | <span data-ttu-id="a93c6-120">Annullert</span><span class="sxs-lookup"><span data-stu-id="a93c6-120">Canceled</span></span> | <span data-ttu-id="a93c6-121">Forespørselen om rekruttering for denne stillingen er avbrutt.</span><span class="sxs-lookup"><span data-stu-id="a93c6-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a93c6-122">Se også</span><span class="sxs-lookup"><span data-stu-id="a93c6-122">See also</span></span>

[<span data-ttu-id="a93c6-123">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="a93c6-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="a93c6-124">Eksempelspørring for rekrutteringsforespørsel</span><span class="sxs-lookup"><span data-stu-id="a93c6-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)
