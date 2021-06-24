---
title: Vise planhistorikk og planleggingslogger
description: Dette emnet forklarer hvordan du viser loggen for planleggingsjobber som utløses av planleggingsoptimaliserings-funksjonaliteten.
author: ChristianRytt
ms.date: 10/30/2019
ms.topic: article
ms.prod: ''
ms.technology: ''
ms.search.form: MPSPlanRegenerationJobList, MPSPlanRegenerationJobLogs
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: d7bba084b03f8698c8bf31d171d5e4e486ed06ad
ms.sourcegitcommit: a7649b361ec54b49c0e9ee1c1c63a8815f320225
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 06/04/2021
ms.locfileid: "6187253"
---
# <a name="view-plan-history-and-planning-logs"></a><span data-ttu-id="e476e-103">Vise planhistorikk og planleggingslogger</span><span class="sxs-lookup"><span data-stu-id="e476e-103">View plan history and planning logs</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="e476e-104">Dette emnet forklarer hvordan du viser loggen for planleggingsjobber som utløses av planleggingsoptimaliserings-funksjonaliteten i Microsoft Dynamics 365 Supply Chain Management.</span><span class="sxs-lookup"><span data-stu-id="e476e-104">This topic explains how to view the history of planning jobs that are triggered by the Planning Optimization functionality in Microsoft Dynamics 365 Supply Chain Management.</span></span>

<span data-ttu-id="e476e-105">Hvis du vil vise loggen for en plan, åpner du planen ved å gå til **Hovedplanlegging** \> **Oppsett** \> **Planer** \> **Hovedplaner** og velge **Historikk**.</span><span class="sxs-lookup"><span data-stu-id="e476e-105">To view the history for a plan, open the plan by going to **Master planning** \> **Setup** \> **Plans** \> **Master plans** and selecting **History**.</span></span> <span data-ttu-id="e476e-106">Loggen viser alle jobbene for den valgte planen.</span><span class="sxs-lookup"><span data-stu-id="e476e-106">The history lists all the jobs for the selected plan.</span></span> <span data-ttu-id="e476e-107">Listen omfatter fullførte og aktive jobber.</span><span class="sxs-lookup"><span data-stu-id="e476e-107">The list includes completed and active jobs.</span></span>

<span data-ttu-id="e476e-108">Loggen for jobber for kjøringer av hovedplanlegging for planleggingsoptimalisering har bare plass til opptil 60 poster per hovedplan.</span><span class="sxs-lookup"><span data-stu-id="e476e-108">The history of jobs for Planning Optimization master planning runs keeps only up to 60 records per master plan.</span></span> <span data-ttu-id="e476e-109">Hver gang du kjører en ny hovedplanleggingsberegning, blir denne planens tidligste loggpost slettet.</span><span class="sxs-lookup"><span data-stu-id="e476e-109">Whenever you run a new master planning calculation, that plan's earliest history record is deleted.</span></span>

<span data-ttu-id="e476e-110">I tillegg til å se starttid og status for jobber, kan du vise loggen for en bestemt jobb.</span><span class="sxs-lookup"><span data-stu-id="e476e-110">In addition to seeing the start time and status of jobs, you can view the log for a specific job.</span></span> <span data-ttu-id="e476e-111">Loggen inneholder tilleggsinformasjon og advarsler.</span><span class="sxs-lookup"><span data-stu-id="e476e-111">The log includes additional information and warnings.</span></span> <span data-ttu-id="e476e-112">Ikke alle jobber har en logg.</span><span class="sxs-lookup"><span data-stu-id="e476e-112">Not all jobs have a log.</span></span> <span data-ttu-id="e476e-113">Hvis du vil vise loggen for en jobb, velger du **Logg**.</span><span class="sxs-lookup"><span data-stu-id="e476e-113">To view the log for a job, select **Log**.</span></span> <span data-ttu-id="e476e-114">Loggoppføringer lagres bare i 30 dager etter avslutningsdatoen for jobben, og deretter slettes de automatisk.</span><span class="sxs-lookup"><span data-stu-id="e476e-114">Log entries are only stored for 30 days after the date the job finished, after that they are automatically deleted.</span></span>

## <a name="related-resources"></a><span data-ttu-id="e476e-115">Relaterte ressurser</span><span class="sxs-lookup"><span data-stu-id="e476e-115">Related resources</span></span>

- [<span data-ttu-id="e476e-116">Oversikt over planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="e476e-116">Planning Optimization overview</span></span>](planning-optimization-overview.md)
- [<span data-ttu-id="e476e-117">Komme i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="e476e-117">Get started with Planning Optimization</span></span>](get-started.md)
- [<span data-ttu-id="e476e-118">Tilpassingsanalyse av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="e476e-118">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)
- [<span data-ttu-id="e476e-119">Bruke filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="e476e-119">Apply filters to a plan</span></span>](plan-filters.md)
- [<span data-ttu-id="e476e-120">Annullere en planleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="e476e-120">Cancel a planning job</span></span>](cancel-planning-job.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]