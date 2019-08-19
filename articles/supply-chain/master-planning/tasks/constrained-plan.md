---
title: Generere en begrenset plan
description: Denne fremgangsmåten viser hvordan du oppretter en plan som tar hensyn til både material- og kapasitetsbegrensninger.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, ReqPlanSched
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 72cddd58b7068e08cddf24df83da8da2f7af7168
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845311"
---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="b775d-103">Generere en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="b775d-103">Generate a constrained plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="b775d-104">Denne fremgangsmåten viser hvordan du oppretter en plan som tar hensyn til både material- og kapasitetsbegrensninger.</span><span class="sxs-lookup"><span data-stu-id="b775d-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="b775d-105">Planen sikrer at produksjonen ikke starter før materialer er tilgjengelige og ressurser er ikke overbestilt.</span><span class="sxs-lookup"><span data-stu-id="b775d-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="b775d-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="b775d-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="b775d-107">Denne fremgangsmåten er ment for produksjonsplanleggeren.</span><span class="sxs-lookup"><span data-stu-id="b775d-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="b775d-108">Definere en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="b775d-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="b775d-109">Klikk Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="b775d-109">Click Master planning.</span></span>
2. <span data-ttu-id="b775d-110">Klikk Hovedplaner.</span><span class="sxs-lookup"><span data-stu-id="b775d-110">Click Master plans.</span></span>
3. <span data-ttu-id="b775d-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="b775d-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="b775d-112">Eksempel: Statisk plan</span><span class="sxs-lookup"><span data-stu-id="b775d-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="b775d-113">Velg Ja i Begrenset kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="b775d-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="b775d-114">Angi 30 i feltet Begrenset kapasitet.</span><span class="sxs-lookup"><span data-stu-id="b775d-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="b775d-115">Utvid horisontene i dager-delen.</span><span class="sxs-lookup"><span data-stu-id="b775d-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="b775d-116">Velg Ja i Kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="b775d-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="b775d-117">Angi et tall i feltet Kapasitetsplanleggingshorisont (dager).</span><span class="sxs-lookup"><span data-stu-id="b775d-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="b775d-118">Eksempel: 60</span><span class="sxs-lookup"><span data-stu-id="b775d-118">Example: 60</span></span>  
9. <span data-ttu-id="b775d-119">Velg Ja i feltet Beregnede forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="b775d-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="b775d-120">Angi et tall i feltet Beregn forsinkelseshorisont (dager).</span><span class="sxs-lookup"><span data-stu-id="b775d-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="b775d-121">Eksempel: 60</span><span class="sxs-lookup"><span data-stu-id="b775d-121">Example: 60</span></span>  
11. <span data-ttu-id="b775d-122">Utvid delen Beregnede forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="b775d-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="b775d-123">Velg Ja i feltet Legg til den beregnede forsinkelsen i behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="b775d-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="b775d-124">Velg Ja i feltet Legg til den beregnede forsinkelsen i behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="b775d-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="b775d-125">Velg Ja i feltet Legg til den beregnede forsinkelsen i behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="b775d-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="b775d-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="b775d-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="b775d-127">Opprette en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="b775d-127">Create a constrained plan</span></span>
1. <span data-ttu-id="b775d-128">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="b775d-128">Click Run.</span></span>
2. <span data-ttu-id="b775d-129">Angi eller velg en verdi i Hovedplan-feltet.</span><span class="sxs-lookup"><span data-stu-id="b775d-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="b775d-130">Velg planen som du har definert begrensninger for.</span><span class="sxs-lookup"><span data-stu-id="b775d-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="b775d-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="b775d-131">Click OK.</span></span>
    * <span data-ttu-id="b775d-132">Dette kan ta en stund.</span><span class="sxs-lookup"><span data-stu-id="b775d-132">This may take a while.</span></span>  
4. <span data-ttu-id="b775d-133">Klikk Planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="b775d-133">Click Planned orders.</span></span>

