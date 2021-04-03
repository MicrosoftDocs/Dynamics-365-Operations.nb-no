---
title: Jobbfritaksstatus
description: I dette emnet beskrives alternativsettet for Jobbfritaksstatus for Dynamics 365 Human Resources.
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
ms.openlocfilehash: 1f211002468384227acb2343ed6cbc6ae2a215d1
ms.sourcegitcommit: 6affb3316be757c99e1fe9c7c7b312b93c483408
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/17/2021
ms.locfileid: "5464458"
---
# <a name="job-exempt-status"></a><span data-ttu-id="407e1-103">Jobbfritaksstatus</span><span class="sxs-lookup"><span data-stu-id="407e1-103">Job exempt status</span></span>

[!include [Applies to Human Resources](../includes/applies-to-hr.md)]

<span data-ttu-id="407e1-104">I dette emnet beskrives alternativsettet for Jobbfritaksstatus for Dynamics 365 Human Resources.</span><span class="sxs-lookup"><span data-stu-id="407e1-104">This topic describes the Job exempt status option set for Dynamics 365 Human Resources.</span></span>

<span data-ttu-id="407e1-105">Fysisk navn: cdm_jobexemptstatus</span><span class="sxs-lookup"><span data-stu-id="407e1-105">Physical name: cdm_jobexemptstatus</span></span>

<span data-ttu-id="407e1-106">Denne opplistingen spesifiserer alternativsettet for fritaksstatusverdier for FLSA-jobb.</span><span class="sxs-lookup"><span data-stu-id="407e1-106">This enumeration specifies the option set for FLSA job exempt status values.</span></span> <span data-ttu-id="407e1-107">Dette finnes i det eksisterende cdm_jobexemptstatus-alternativsett.</span><span class="sxs-lookup"><span data-stu-id="407e1-107">This is provided in the existing cdm_jobexemptstatus option set.</span></span>

| <span data-ttu-id="407e1-108">Verdi</span><span class="sxs-lookup"><span data-stu-id="407e1-108">Value</span></span> | <span data-ttu-id="407e1-109">Etikett</span><span class="sxs-lookup"><span data-stu-id="407e1-109">Label</span></span> | <span data-ttu-id="407e1-110">beskrivelse</span><span class="sxs-lookup"><span data-stu-id="407e1-110">Description</span></span> |
| --- | --- | --- |
| <span data-ttu-id="407e1-111">200000000</span><span class="sxs-lookup"><span data-stu-id="407e1-111">200000000</span></span> | <span data-ttu-id="407e1-112">Avgiftsfri</span><span class="sxs-lookup"><span data-stu-id="407e1-112">Exempt</span></span> | <span data-ttu-id="407e1-113">Jobben har en fritaksstatus basert på FLSA-retningslinjene.</span><span class="sxs-lookup"><span data-stu-id="407e1-113">The job has an exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="407e1-114">200000001</span><span class="sxs-lookup"><span data-stu-id="407e1-114">200000001</span></span> | <span data-ttu-id="407e1-115">NonExempt</span><span class="sxs-lookup"><span data-stu-id="407e1-115">NonExempt</span></span> | <span data-ttu-id="407e1-116">Jobben har en ikke-fritaksstatus basert på FLSA-retningslinjene.</span><span class="sxs-lookup"><span data-stu-id="407e1-116">The job has a non-exempt status based on FLSA guidelines.</span></span> |
| <span data-ttu-id="407e1-117">200000002</span><span class="sxs-lookup"><span data-stu-id="407e1-117">200000002</span></span> | <span data-ttu-id="407e1-118">Gjelder ikke</span><span class="sxs-lookup"><span data-stu-id="407e1-118">Does Not Apply</span></span> | <span data-ttu-id="407e1-119">FLSA-statusretningslinjer gjelder ikke for jobben.</span><span class="sxs-lookup"><span data-stu-id="407e1-119">FLSA status guidelines do not apply to the job.</span></span> |

## <a name="see-also"></a><span data-ttu-id="407e1-120">Se også</span><span class="sxs-lookup"><span data-stu-id="407e1-120">See also</span></span>

[<span data-ttu-id="407e1-121">Innføring i API for søkersporingssystemintegrering</span><span class="sxs-lookup"><span data-stu-id="407e1-121">Applicant Tracking System integration API introduction</span></span>](hr-admin-integration-ats-api-introduction.md)<br>
[<span data-ttu-id="407e1-122">Eksempelspørring for rekrutteringsforespørsel</span><span class="sxs-lookup"><span data-stu-id="407e1-122">Example query for Recruiting request</span></span>](hr-admin-integration-ats-api-recruiting-request-example-query.md)


[!INCLUDE[footer-include](../includes/footer-banner.md)]