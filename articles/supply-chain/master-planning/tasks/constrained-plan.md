---
title: Generere en begrenset plan
description: Dette emnet forklarer hvordan du oppretter en plan som tar hensyn til både material- og kapasitetsbegrensninger.
author: ShylaThompson
manager: tfehr
ms.date: 08/02/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d8b9d5712dd1b4f9958de775e1a2224b64485d05
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3987220"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="bc54c-103">Generere en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="bc54c-103">Generate a constrained plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="bc54c-104">Dette emnet forklarer hvordan du oppretter en plan som tar hensyn til både material- og kapasitetsbegrensninger.</span><span class="sxs-lookup"><span data-stu-id="bc54c-104">This topic explains how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="bc54c-105">Planen sikrer at produksjonen ikke starter før materialer er tilgjengelige og ressurser er ikke overbestilt.</span><span class="sxs-lookup"><span data-stu-id="bc54c-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="bc54c-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="bc54c-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="bc54c-107">Denne fremgangsmåten er ment for produksjonsplanleggeren.</span><span class="sxs-lookup"><span data-stu-id="bc54c-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="bc54c-108">Definere en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="bc54c-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="bc54c-109">Velg arbeidsområdet **Hovedplanlegging** på startsiden.</span><span class="sxs-lookup"><span data-stu-id="bc54c-109">In the home page, select the **Master planning** workspace.</span></span>
2. <span data-ttu-id="bc54c-110">Velg **Hovedplaner** i listen over koblinger helt til høyre på siden i arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="bc54c-110">Select **Master plans** in the list of links on the far right side of the workspace.</span></span>
3. <span data-ttu-id="bc54c-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="bc54c-111">In the list, find and select the desired record.</span></span> <span data-ttu-id="bc54c-112">Eksempel: **Statisk plan**</span><span class="sxs-lookup"><span data-stu-id="bc54c-112">Example: **StaticPlan**</span></span>  
4. <span data-ttu-id="bc54c-113">Velg **Ja** i **Begrenset kapasitet** -feltet.</span><span class="sxs-lookup"><span data-stu-id="bc54c-113">Select **Yes** in the **Finite capacity** field.</span></span>
5. <span data-ttu-id="bc54c-114">I feltet **Horisont for begrenset kapasitet** angir du `30`.</span><span class="sxs-lookup"><span data-stu-id="bc54c-114">In the **Finite capacity time fence** field, enter `30`.</span></span>
6. <span data-ttu-id="bc54c-115">Utvid delen **Horisonter i dager** .</span><span class="sxs-lookup"><span data-stu-id="bc54c-115">Expand the **Time fences in days** section.</span></span>
7. <span data-ttu-id="bc54c-116">Velg **Ja** i **Kapasitet** -feltet.</span><span class="sxs-lookup"><span data-stu-id="bc54c-116">Select **Yes** in the **Capacity** field.</span></span>
8. <span data-ttu-id="bc54c-117">Angi et tall i feltet **Kapasitetsplanleggingshorisont (dager)** .</span><span class="sxs-lookup"><span data-stu-id="bc54c-117">In the **Capacity scheduling time fence (days)** field, enter a number.</span></span> <span data-ttu-id="bc54c-118">Eksempel: `60`</span><span class="sxs-lookup"><span data-stu-id="bc54c-118">Example: `60`</span></span>  
9. <span data-ttu-id="bc54c-119">Velg **Ja** i feltet **Beregnede forsinkelser** .</span><span class="sxs-lookup"><span data-stu-id="bc54c-119">Select **Yes** in the **Calculated delays** field.</span></span>
10. <span data-ttu-id="bc54c-120">Angi et tall i feltet **Beregn forsinkelseshorisont (dager)** .</span><span class="sxs-lookup"><span data-stu-id="bc54c-120">In the **Calculate delays time fence (days)** field, enter a number.</span></span> <span data-ttu-id="bc54c-121">Eksempel: `60`</span><span class="sxs-lookup"><span data-stu-id="bc54c-121">Example: `60`</span></span> 
11. <span data-ttu-id="bc54c-122">Utvid delen **Beregnede forsinkelser** .</span><span class="sxs-lookup"><span data-stu-id="bc54c-122">Expand the **Calculated delays** section.</span></span>
12. <span data-ttu-id="bc54c-123">Velg **Ja** i alle felt kalt **Legg til den beregnede forsinkelsen i behovsdatoen** .</span><span class="sxs-lookup"><span data-stu-id="bc54c-123">Select **Yes** in all **Add the calculated delay to the requirement date** fields.</span></span>
13. <span data-ttu-id="bc54c-124">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="bc54c-124">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="bc54c-125">Opprette en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="bc54c-125">Create a constrained plan</span></span>
1. <span data-ttu-id="bc54c-126">Velg **Kjør** .</span><span class="sxs-lookup"><span data-stu-id="bc54c-126">Select **Run** .</span></span>
2. <span data-ttu-id="bc54c-127">I **Hovedplan** -feltet angir eller velger du planen du har definert betingelser for.</span><span class="sxs-lookup"><span data-stu-id="bc54c-127">In the **Master plan** field, enter or select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="bc54c-128">Velg **OK** .</span><span class="sxs-lookup"><span data-stu-id="bc54c-128">Select **OK** .</span></span>
4. <span data-ttu-id="bc54c-129">Velg **Planlagte ordrer** .</span><span class="sxs-lookup"><span data-stu-id="bc54c-129">Select **Planned orders** .</span></span>

