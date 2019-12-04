---
title: Annullere en planleggingsjobb
description: Dette emnet beskriver hvordan du avbryter en aktiv planleggingsjobb som bruker planleggingsoptimaliserings-funksjonaliteten.
author: ChristianRytt
manager: AnnBe
ms.date: 10/26/2019
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: a2d90f04985fdd66ca83582ee676100fffb26981
ms.sourcegitcommit: fbc106af09bdadb860677f590464fb93223cbf65
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 11/06/2019
ms.locfileid: "2774024"
---
[!include [banner](../../includes/banner.md)]
[!include [banner](../../includes/preview-banner.md)]

# <a name="cancel-a-planning-job"></a><span data-ttu-id="375e0-103">Annullere en planleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="375e0-103">Cancel a planning job</span></span>

<span data-ttu-id="375e0-104">I Microsoft Dynamics 365 Supply Chain Management kan du avbryte en aktiv planleggingsjobb som bruker planleggingsoptimaliserings-funksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="375e0-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning Optimization functionality.</span></span>

<span data-ttu-id="375e0-105">Hvis du vil avbryte en aktiv planleggingsjobb, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="375e0-105">To cancel an active planning job, follow these steps.</span></span>

> [!NOTE]
> <span data-ttu-id="375e0-106">Bare aktive jobber kan avbrytes.</span><span class="sxs-lookup"><span data-stu-id="375e0-106">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="375e0-107">Gå til **Hovedplanlegging \> Oppsett \> Planer**.</span><span class="sxs-lookup"><span data-stu-id="375e0-107">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="375e0-108">Velg en passende plan for planleggingskjøringen.</span><span class="sxs-lookup"><span data-stu-id="375e0-108">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="375e0-109">Velg **Logg**.</span><span class="sxs-lookup"><span data-stu-id="375e0-109">Select **History**.</span></span>
4. <span data-ttu-id="375e0-110">Velg planleggingsjobben som skal avbrytes.</span><span class="sxs-lookup"><span data-stu-id="375e0-110">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="375e0-111">Velg **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="375e0-111">Select **Cancel**.</span></span>

<span data-ttu-id="375e0-112">Jobbstatusen blir **Avbryter** til planleggingsoptimaliserings-tjenesten bekrefter at jobben er avbrutt.</span><span class="sxs-lookup"><span data-stu-id="375e0-112">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="375e0-113">Da vil statusen bli endret til **Avbrutt**.</span><span class="sxs-lookup"><span data-stu-id="375e0-113">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="375e0-114">Hvis du vil vise statusendringer, må du oppdatere siden ved å velge **Oppdater**-knappen.</span><span class="sxs-lookup"><span data-stu-id="375e0-114">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="related-resources"></a><span data-ttu-id="375e0-115">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="375e0-115">Related resources</span></span>

[<span data-ttu-id="375e0-116">Oversikt over planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="375e0-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="375e0-117">Kom i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="375e0-117">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="375e0-118">Tilpassingsanalyse av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="375e0-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="375e0-119">Vise planhistorikk og planleggingslogger</span><span class="sxs-lookup"><span data-stu-id="375e0-119">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="375e0-120">Bruke filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="375e0-120">Apply filters to a plan</span></span>](plan-filters.md)
