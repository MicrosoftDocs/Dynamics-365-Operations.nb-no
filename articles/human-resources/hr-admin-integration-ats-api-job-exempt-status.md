---
title: Jobbfritaksstatus
description: I dette emnet beskrives alternativsettet for Jobbfritaksstatus for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 4765858f389f28467ae2ac71084c15d2ba0cbe8b
ms.sourcegitcommit: 3cdc42346bb653c13ab33a7142dbb7969f1f6dda
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/31/2021
ms.locfileid: "5798303"
---
# <a name="job-exempt-status"></a><span data-ttu-id="c7f29-103">Jobbfritaksstatus</span><span class="sxs-lookup"><span data-stu-id="c7f29-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="c7f29-104">I dette emnet beskrives alternativsettet for Jobbfritaksstatus for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="c7f29-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="c7f29-105">Fysisk navn: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="c7f29-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="c7f29-106">Denne opplistingen spesifiserer alternativsettet for fritaksstatusverdier for FLSA-jobb.</span><span class="sxs-lookup"><span data-stu-id="c7f29-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="c7f29-107">Dette finnes i det eksisterende cdm_jobexemptstatus-alternativsett.</span><span class="sxs-lookup"><span data-stu-id="c7f29-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="c7f29-108">Verdi</span><span class="sxs-lookup"><span data-stu-id="c7f29-108">Value</span></span> | <span data-ttu-id="c7f29-109">Etikett</span><span class="sxs-lookup"><span data-stu-id="c7f29-109">Label</span></span> | <span data-ttu-id="c7f29-110">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="c7f29-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="c7f29-111">200000000</span><span class="sxs-lookup"><span data-stu-id="c7f29-111">200000000</span></span> | <span data-ttu-id="c7f29-112">Avgiftsfri</span><span class="sxs-lookup"><span data-stu-id="c7f29-112">Exempt</span></span> | <span data-ttu-id="c7f29-113">Jobben har en fritaksstatus basert på FLSA-retningslinjene.</span><span class="sxs-lookup"><span data-stu-id="c7f29-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="c7f29-114">200000001</span><span class="sxs-lookup"><span data-stu-id="c7f29-114">200000001</span></span> | <span data-ttu-id="c7f29-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="c7f29-115">NonExempt</span></span> | <span data-ttu-id="c7f29-116">Jobben har en ikke-fritaksstatus basert på FLSA-retningslinjene.</span><span class="sxs-lookup"><span data-stu-id="c7f29-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="c7f29-117">200000002</span><span class="sxs-lookup"><span data-stu-id="c7f29-117">200000002</span></span> | <span data-ttu-id="c7f29-118">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="c7f29-118">Does Not Apply</span></span> | <span data-ttu-id="c7f29-119">FLSA-statusretningslinjer gjelder ikke for jobben.</span><span class="sxs-lookup"><span data-stu-id="c7f29-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="c7f29-120">Se også</span><span class="sxs-lookup"><span data-stu-id="c7f29-120">See also</span></span>

[<span data-ttu-id="c7f29-121">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="c7f29-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="c7f29-122">Eksempelspørring for rekrutteringsforespørsel</span><span class="sxs-lookup"><span data-stu-id="c7f29-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]