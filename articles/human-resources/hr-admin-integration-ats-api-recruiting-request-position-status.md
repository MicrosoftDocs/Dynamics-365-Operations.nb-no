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
ms.openlocfilehash: 01e8aa5157d0ad1c01f996886e7845e49ab97603
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464724"
---
# <a name="recruiting-request-position-status"></a><span data-ttu-id="fad67-103">Status for rekrutteringsforespørselsstilling</span><span class="sxs-lookup"><span data-stu-id="fad67-103">Recruiting request position status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="fad67-104">Dette emnet beskriver status for stillingen i en rekrutteringsforespørsel for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="fad67-104">This topic describes the Recruiting request position status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="fad67-105">Fysisk navn: mshr_hcmrecruitingrequestpositionstatus</span><span class="sxs-lookup"><span data-stu-id="fad67-105">Physical name: mshr_hcmrecruitingrequestpositionstatus</span></span>

<span data-ttu-id="fad67-106">Denne opplistingen gir alternativetsett for statusverdiene til hver stilling en rekrutteringsforespørsel i RecruitingRequestPosition-enheten.</span><span class="sxs-lookup"><span data-stu-id="fad67-106">This enumeration provides the option set for the status values of each position a recruiting request in the RecruitingRequestPosition entity.</span></span>

| <span data-ttu-id="fad67-107">Verdi</span><span class="sxs-lookup"><span data-stu-id="fad67-107">Value</span></span> | <span data-ttu-id="fad67-108">Etikett</span><span class="sxs-lookup"><span data-stu-id="fad67-108">Label</span></span> | <span data-ttu-id="fad67-109">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="fad67-109">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="fad67-110">200000000</span><span class="sxs-lookup"><span data-stu-id="fad67-110">200000000</span></span> | <span data-ttu-id="fad67-111">Åpen</span><span class="sxs-lookup"><span data-stu-id="fad67-111">Open</span></span> | <span data-ttu-id="fad67-112">Stillingen i rekrutteringsforespørselen er åpen for rekruttering.</span><span class="sxs-lookup"><span data-stu-id="fad67-112">The position in the recruiting request is open for recruiting.</span></span> <span data-ttu-id="fad67-113">Dette viser ikke at det for øyeblikket ikke er noen aktiv stillingstilordning for stillingen.</span><span class="sxs-lookup"><span data-stu-id="fad67-113">This does not indicate that there is no currently active position assignment for the position.</span></span> <span data-ttu-id="fad67-114">Det kan være en ansatt i stillingen når rekrutteringen gjøres.</span><span class="sxs-lookup"><span data-stu-id="fad67-114">There may be an employee in the position at the time of recruiting.</span></span> <span data-ttu-id="fad67-115">Den viser bare at stillingen er tilgjengelig for rekruttering i konteksten med rekrutteringsforespørselen.</span><span class="sxs-lookup"><span data-stu-id="fad67-115">It indicates only that the position is available for recruiting in the context of the recruiting request.</span></span> |
| <span data-ttu-id="fad67-116">200000001</span><span class="sxs-lookup"><span data-stu-id="fad67-116">200000001</span></span> | <span data-ttu-id="fad67-117">Besatt</span><span class="sxs-lookup"><span data-stu-id="fad67-117">Filled</span></span> | <span data-ttu-id="fad67-118">En arbeider er valgt for tilordning til stillingen.</span><span class="sxs-lookup"><span data-stu-id="fad67-118">A worker has been selected for assignment to the position.</span></span> |
| <span data-ttu-id="fad67-119">200000002</span><span class="sxs-lookup"><span data-stu-id="fad67-119">200000002</span></span> | <span data-ttu-id="fad67-120">Annullert</span><span class="sxs-lookup"><span data-stu-id="fad67-120">Canceled</span></span> | <span data-ttu-id="fad67-121">Forespørselen om rekruttering for denne stillingen er avbrutt.</span><span class="sxs-lookup"><span data-stu-id="fad67-121">The request to recruit for this position has been canceled.</span></span> |

## <a name="see-also"></a><span data-ttu-id="fad67-122">Se også</span><span class="sxs-lookup"><span data-stu-id="fad67-122">See also</span></span>

[<span data-ttu-id="fad67-123">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="fad67-123">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="fad67-124">Eksempelspørring for rekrutteringsforespørsel</span><span class="sxs-lookup"><span data-stu-id="fad67-124">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]