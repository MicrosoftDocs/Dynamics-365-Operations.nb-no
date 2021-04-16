---
title: Status for rekrutteringsforespørselsstilling
description: Dette emnet beskriver status for stillingen i en rekrutteringsforespørsel for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 7e59e9381fb15b339095d6a71296813e0141e9ab
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5789738"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="ff2bd-103">Status for rekrutteringsforespørselsstilling</span><span class="sxs-lookup"><span data-stu-id="ff2bd-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="ff2bd-104">Dette emnet beskriver status for stillingen i en rekrutteringsforespørsel for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="ff2bd-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="ff2bd-105">Fysisk navn: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="ff2bd-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="ff2bd-106">Denne opplistingen gir alternativetsett for statusverdiene til hver stilling en rekrutteringsforespørsel i RecruitingRequestPosition-enheten.</span><span class="sxs-lookup"><span data-stu-id="ff2bd-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="ff2bd-107">Verdi</span><span class="sxs-lookup"><span data-stu-id="ff2bd-107">Value</span></span> | <span data-ttu-id="ff2bd-108">Etikett</span><span class="sxs-lookup"><span data-stu-id="ff2bd-108">Label</span></span> | <span data-ttu-id="ff2bd-109">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="ff2bd-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="ff2bd-110">200000000</span><span class="sxs-lookup"><span data-stu-id="ff2bd-110">200000000</span></span> | <span data-ttu-id="ff2bd-111">Åpen</span><span class="sxs-lookup"><span data-stu-id="ff2bd-111">Open</span></span> | <span data-ttu-id="ff2bd-112">Stillingen i rekrutteringsforespørselen er åpen for rekruttering.</span><span class="sxs-lookup"><span data-stu-id="ff2bd-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="ff2bd-113">Dette viser ikke at det for øyeblikket ikke er noen aktiv stillingstilordning for stillingen.</span><span class="sxs-lookup"><span data-stu-id="ff2bd-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="ff2bd-114">Det kan være en ansatt i stillingen når rekrutteringen gjøres.</span><span class="sxs-lookup"><span data-stu-id="ff2bd-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="ff2bd-115">Den viser bare at stillingen er tilgjengelig for rekruttering i konteksten med rekrutteringsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="ff2bd-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="ff2bd-116">200000001</span><span class="sxs-lookup"><span data-stu-id="ff2bd-116">200000001</span></span> | <span data-ttu-id="ff2bd-117">Besatt</span><span class="sxs-lookup"><span data-stu-id="ff2bd-117">Filled</span></span> | <span data-ttu-id="ff2bd-118">En arbeider er valgt for tilordning til stillingen.</span><span class="sxs-lookup"><span data-stu-id="ff2bd-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="ff2bd-119">200000002</span><span class="sxs-lookup"><span data-stu-id="ff2bd-119">200000002</span></span> | <span data-ttu-id="ff2bd-120">Annullert</span><span class="sxs-lookup"><span data-stu-id="ff2bd-120">Canceled</span></span> | <span data-ttu-id="ff2bd-121">Forespørselen om rekruttering for denne stillingen er avbrutt.</span><span class="sxs-lookup"><span data-stu-id="ff2bd-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="ff2bd-122">Se også</span><span class="sxs-lookup"><span data-stu-id="ff2bd-122">See also</span></span>

[<span data-ttu-id="ff2bd-123">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="ff2bd-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="ff2bd-124">Eksempelspørring for rekrutteringsforespørsel</span><span class="sxs-lookup"><span data-stu-id="ff2bd-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]