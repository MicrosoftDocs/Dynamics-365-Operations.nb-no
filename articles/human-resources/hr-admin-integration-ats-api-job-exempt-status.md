---
title: Jobbfritaksstatus
description: I dette emnet beskrives alternativsettet for Jobbfritaksstatus for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 8e91fbb420009d5131e2faa7dbea8a302a027e0a
ms.sourcegitcommit: 879ee8a10e6158885795dce4b3db5077540eec41
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/18/2021
ms.locfileid: "6053857"
---
# <a name="job-exempt-status"></a><span data-ttu-id="a57d6-103">Jobbfritaksstatus</span><span class="sxs-lookup"><span data-stu-id="a57d6-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="a57d6-104">I dette emnet beskrives alternativsettet for Jobbfritaksstatus for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="a57d6-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="a57d6-105">Fysisk navn: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="a57d6-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="a57d6-106">Denne opplistingen spesifiserer alternativsettet for fritaksstatusverdier for FLSA-jobb.</span><span class="sxs-lookup"><span data-stu-id="a57d6-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="a57d6-107">Dette finnes i det eksisterende cdm_jobexemptstatus-alternativsett.</span><span class="sxs-lookup"><span data-stu-id="a57d6-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="a57d6-108">Verdi</span><span class="sxs-lookup"><span data-stu-id="a57d6-108">Value</span></span> | <span data-ttu-id="a57d6-109">Etikett</span><span class="sxs-lookup"><span data-stu-id="a57d6-109">Label</span></span> | <span data-ttu-id="a57d6-110">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="a57d6-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="a57d6-111">200000000</span><span class="sxs-lookup"><span data-stu-id="a57d6-111">200000000</span></span> | <span data-ttu-id="a57d6-112">Avgiftsfri</span><span class="sxs-lookup"><span data-stu-id="a57d6-112">Exempt</span></span> | <span data-ttu-id="a57d6-113">Jobben har en fritaksstatus basert på FLSA-retningslinjene.</span><span class="sxs-lookup"><span data-stu-id="a57d6-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="a57d6-114">200000001</span><span class="sxs-lookup"><span data-stu-id="a57d6-114">200000001</span></span> | <span data-ttu-id="a57d6-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="a57d6-115">NonExempt</span></span> | <span data-ttu-id="a57d6-116">Jobben har en ikke-fritaksstatus basert på FLSA-retningslinjene.</span><span class="sxs-lookup"><span data-stu-id="a57d6-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="a57d6-117">200000002</span><span class="sxs-lookup"><span data-stu-id="a57d6-117">200000002</span></span> | <span data-ttu-id="a57d6-118">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="a57d6-118">Does Not Apply</span></span> | <span data-ttu-id="a57d6-119">FLSA-statusretningslinjer gjelder ikke for jobben.</span><span class="sxs-lookup"><span data-stu-id="a57d6-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="a57d6-120">Se også</span><span class="sxs-lookup"><span data-stu-id="a57d6-120">See also</span></span>

[<span data-ttu-id="a57d6-121">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="a57d6-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="a57d6-122">Eksempelspørring for rekrutteringsforespørsel</span><span class="sxs-lookup"><span data-stu-id="a57d6-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]