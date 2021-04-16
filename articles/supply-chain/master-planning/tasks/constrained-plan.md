---
title: Generere en begrenset plan
description: Dette emnet forklarer hvordan du oppretter en plan som tar hensyn til både material- og kapasitetsbegrensninger.
author: ShylaThompson
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c35d5a7465cc6cfe0bc12cb00796eff2aeed1ece
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5808022"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="13dbe-103">Generere en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="13dbe-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="13dbe-104">Dette emnet forklarer hvordan du oppretter en plan som tar hensyn til både material- og kapasitetsbegrensninger.</span><span class="sxs-lookup"><span data-stu-id="13dbe-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="13dbe-105">Planen sikrer at produksjonen ikke starter før materialer er tilgjengelige og ressurser er ikke overbestilt.</span><span class="sxs-lookup"><span data-stu-id="13dbe-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="13dbe-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="13dbe-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="13dbe-107">Denne fremgangsmåten er ment for produksjonsplanleggeren.</span><span class="sxs-lookup"><span data-stu-id="13dbe-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="13dbe-108">Definere en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="13dbe-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="13dbe-109">Velg arbeidsområdet **Hovedplanlegging** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="13dbe-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="13dbe-110">Velg **Hovedplaner** i listen over koblinger helt til høyre på siden i arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="13dbe-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="13dbe-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="13dbe-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="13dbe-112">Eksempel: **Statisk plan**</span><span class="sxs-lookup"><span data-stu-id="13dbe-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="13dbe-113">Velg **Ja** i **Begrenset kapasitet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="13dbe-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="13dbe-114">I feltet **Horisont for begrenset kapasitet** angir du `30`.</span><span class="sxs-lookup"><span data-stu-id="13dbe-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="13dbe-115">Utvid delen **Horisonter i dager**.</span><span class="sxs-lookup"><span data-stu-id="13dbe-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="13dbe-116">Velg **Ja** i **Kapasitet**-feltet.</span><span class="sxs-lookup"><span data-stu-id="13dbe-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="13dbe-117">Angi et tall i feltet **Kapasitetsplanleggingshorisont (dager)**.</span><span class="sxs-lookup"><span data-stu-id="13dbe-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="13dbe-118">Eksempel: `60`</span><span class="sxs-lookup"><span data-stu-id="13dbe-118">Example: `60`</span></span>  
9. <span data-ttu-id="13dbe-119">Velg **Ja** i feltet **Beregnede forsinkelser**.</span><span class="sxs-lookup"><span data-stu-id="13dbe-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="13dbe-120">Angi et tall i feltet **Beregn forsinkelseshorisont (dager)**.</span><span class="sxs-lookup"><span data-stu-id="13dbe-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="13dbe-121">Eksempel: `60`</span><span class="sxs-lookup"><span data-stu-id="13dbe-121">Example: `60`</span></span> 
11. <span data-ttu-id="13dbe-122">Utvid delen **Beregnede forsinkelser**.</span><span class="sxs-lookup"><span data-stu-id="13dbe-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="13dbe-123">Velg **Ja** i alle felt kalt **Legg til den beregnede forsinkelsen i behovsdatoen**.</span><span class="sxs-lookup"><span data-stu-id="13dbe-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="13dbe-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="13dbe-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="13dbe-125">Opprette en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="13dbe-125">Create a constrained plan</span></span>
1. <span data-ttu-id="13dbe-126">Velg **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="13dbe-126">Select **Run**.</span></span>
2. <span data-ttu-id="13dbe-127">I **Hovedplan**-feltet angir eller velger du planen du har definert betingelser for.</span><span class="sxs-lookup"><span data-stu-id="13dbe-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="13dbe-128">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="13dbe-128">Select **OK**.</span></span>
4. <span data-ttu-id="13dbe-129">Velg **Planlagte ordrer**.</span><span class="sxs-lookup"><span data-stu-id="13dbe-129">Select **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]