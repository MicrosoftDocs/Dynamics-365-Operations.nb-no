---
title: Annullere en planleggingsjobb
description: Dette emnet beskriver hvordan du avbryter en aktiv planleggingsjobb som bruker planleggingsoptimaliserings-funksjonaliteten.
author: ChristianRytt
manager: tfehr
ms.date: 02/18/2020
ms.topic: article
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.custom: ''
ms.assetid: ''
ms.search.region: Global
ms.search.industry: Manufacturing
ms.author: crytt
ms.search.validFrom: 2019-10-31
ms.dyn365.ops.version: AX 10.0.5
ms.openlocfilehash: 5aadf7fb94bb2d836892064837f9cb1c5790d657
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5238020"
---
# <a name="cancel-a-planning-job"></a><span data-ttu-id="50a8e-103">Avbryte en planleggingsjobb</span><span class="sxs-lookup"><span data-stu-id="50a8e-103">Cancel a planning job</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="50a8e-104">I Microsoft Dynamics 365 Supply Chain Management kan du avbryte en aktiv planleggingsjobb som bruker planleggingsoptimaliserings-funksjonaliteten.</span><span class="sxs-lookup"><span data-stu-id="50a8e-104">In Microsoft Dynamics 365 Supply Chain Management, you can cancel an active planning job that uses the Planning optimization functionality.</span></span> <span data-ttu-id="50a8e-105">Når du velger **Avbryt** i dialogboksen når en planleggingsoptimaliseringsjobb utløses direkte fra brukergrensesnittet (ikke i bakgrunnen), vil ikke dette avbryte planleggingsoptimaliseringsjobben.</span><span class="sxs-lookup"><span data-stu-id="50a8e-105">When you select **Cancel** in the dialog box when a Planning optimization job is triggered directly from the user interface (not in the background), this will not cancel the Planning optimization job.</span></span> <span data-ttu-id="50a8e-106">Selv om du får en advarsel som "operasjonen er avbrutt", må du likevel bruke følgende fremgangsmåte for å avbryte en planleggingsjobb med planleggingsoptimalisering.</span><span class="sxs-lookup"><span data-stu-id="50a8e-106">Even if you receive a warning such as “Operation canceled”, you will still need to use the following steps to cancel a planning job with Planning optimization.</span></span>


<span data-ttu-id="50a8e-107">Hvis du vil avbryte en aktiv planleggingsjobb, følger du disse trinnene.</span><span class="sxs-lookup"><span data-stu-id="50a8e-107">To cancel an active planning job, follow these steps.</span></span> 

> [!NOTE]
> <span data-ttu-id="50a8e-108">Bare aktive jobber kan avbrytes.</span><span class="sxs-lookup"><span data-stu-id="50a8e-108">Only active jobs can be canceled.</span></span>

1. <span data-ttu-id="50a8e-109">Gå til **Hovedplanlegging \> Oppsett \> Planer**.</span><span class="sxs-lookup"><span data-stu-id="50a8e-109">Go to **Master planning \> Setup \> Plans**.</span></span>
2. <span data-ttu-id="50a8e-110">Velg en passende plan for planleggingskjøringen.</span><span class="sxs-lookup"><span data-stu-id="50a8e-110">Select an appropriate plan for the planning run.</span></span>
3. <span data-ttu-id="50a8e-111">Velg **Logg**.</span><span class="sxs-lookup"><span data-stu-id="50a8e-111">Select **History**.</span></span>
4. <span data-ttu-id="50a8e-112">Velg planleggingsjobben som skal avbrytes.</span><span class="sxs-lookup"><span data-stu-id="50a8e-112">Select the planning job to cancel.</span></span>
5. <span data-ttu-id="50a8e-113">Velg **Avbryt**.</span><span class="sxs-lookup"><span data-stu-id="50a8e-113">Select **Cancel**.</span></span>

<span data-ttu-id="50a8e-114">Jobbstatusen blir **Avbryter** til planleggingsoptimaliserings-tjenesten bekrefter at jobben er avbrutt.</span><span class="sxs-lookup"><span data-stu-id="50a8e-114">The job status will be **Canceling** until the Planning Optimization service confirms that the job has been canceled.</span></span> <span data-ttu-id="50a8e-115">Da vil statusen bli endret til **Avbrutt**.</span><span class="sxs-lookup"><span data-stu-id="50a8e-115">The status will then be changed to **Canceled**.</span></span>

> [!NOTE]
> <span data-ttu-id="50a8e-116">Hvis du vil vise statusendringer, må du oppdatere siden ved å velge **Oppdater**-knappen.</span><span class="sxs-lookup"><span data-stu-id="50a8e-116">To see status changes, you must refresh the page by selecting the **Refresh** button.</span></span>

## <a name="additional-resources"></a><span data-ttu-id="50a8e-117">Tilleggsressurser</span><span class="sxs-lookup"><span data-stu-id="50a8e-117">Additional resources</span></span>

[<span data-ttu-id="50a8e-118">Oversikt over planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="50a8e-118">Planning Optimization overview</span></span>](planning-optimization-overview.md)

[<span data-ttu-id="50a8e-119">Komme i gang med planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="50a8e-119">Get started with Planning Optimization</span></span>](get-started.md)

[<span data-ttu-id="50a8e-120">Tilpassingsanalyse av planleggingsoptimalisering</span><span class="sxs-lookup"><span data-stu-id="50a8e-120">Planning Optimization fit analysis</span></span>](planning-optimization-fit-analysis.md)

[<span data-ttu-id="50a8e-121">Vise planhistorikk og planleggingslogger</span><span class="sxs-lookup"><span data-stu-id="50a8e-121">View plan history and planning logs</span></span>](plan-history-logs.md)

[<span data-ttu-id="50a8e-122">Bruke filtre på en plan</span><span class="sxs-lookup"><span data-stu-id="50a8e-122">Apply filters to a plan</span></span>](plan-filters.md)


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]