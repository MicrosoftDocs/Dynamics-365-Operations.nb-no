--- 
title: Generere en begrenset plan
description: "Denne fremgangsmåten viser hvordan du oppretter en plan som tar hensyn til både material- og kapasitetsbegrensninger."
author: YuyuScheller
manager: AnnBe
ms.date: 03/02/2016
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 9deb615d05b90865ea6a050599bf91879b5688d0
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="d9898-103">Generere en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="d9898-103">Generate a constrained plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="d9898-104">Denne fremgangsmåten viser hvordan du oppretter en plan som tar hensyn til både material- og kapasitetsbegrensninger.</span><span class="sxs-lookup"><span data-stu-id="d9898-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="d9898-105">Planen sikrer at produksjonen ikke starter før materialer er tilgjengelige og ressurser er ikke overbestilt.</span><span class="sxs-lookup"><span data-stu-id="d9898-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="d9898-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="d9898-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="d9898-107">Denne fremgangsmåten er ment for produksjonsplanleggeren.</span><span class="sxs-lookup"><span data-stu-id="d9898-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="d9898-108">Definere en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="d9898-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="d9898-109">Klikk Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="d9898-109">Click Master planning.</span></span>
2. <span data-ttu-id="d9898-110">Klikk Hovedplaner.</span><span class="sxs-lookup"><span data-stu-id="d9898-110">Click Master plans.</span></span>
3. <span data-ttu-id="d9898-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="d9898-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="d9898-112">Eksempel: Statisk plan</span><span class="sxs-lookup"><span data-stu-id="d9898-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="d9898-113">Velg Ja i Begrenset kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="d9898-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="d9898-114">Angi 30 i feltet Begrenset kapasitet.</span><span class="sxs-lookup"><span data-stu-id="d9898-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="d9898-115">Utvid horisontene i dager-delen.</span><span class="sxs-lookup"><span data-stu-id="d9898-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="d9898-116">Velg Ja i Kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="d9898-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="d9898-117">Angi et tall i feltet Kapasitetsplanleggingshorisont (dager).</span><span class="sxs-lookup"><span data-stu-id="d9898-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="d9898-118">Eksempel: 60</span><span class="sxs-lookup"><span data-stu-id="d9898-118">Example: 60</span></span>  
9. <span data-ttu-id="d9898-119">Velg Ja i feltet Beregnede forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="d9898-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="d9898-120">Angi et tall i feltet Beregn forsinkelseshorisont (dager).</span><span class="sxs-lookup"><span data-stu-id="d9898-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="d9898-121">Eksempel: 60</span><span class="sxs-lookup"><span data-stu-id="d9898-121">Example: 60</span></span>  
11. <span data-ttu-id="d9898-122">Utvid delen Beregnede forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="d9898-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="d9898-123">Velg Ja i feltet Legg til den beregnede forsinkelsen i behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="d9898-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="d9898-124">Velg Ja i feltet Legg til den beregnede forsinkelsen i behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="d9898-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="d9898-125">Velg Ja i feltet Legg til den beregnede forsinkelsen i behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="d9898-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="d9898-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="d9898-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="d9898-127">Opprette en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="d9898-127">Create a constrained plan</span></span>
1. <span data-ttu-id="d9898-128">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="d9898-128">Click Run.</span></span>
2. <span data-ttu-id="d9898-129">Angi eller velg en verdi i Hovedplan-feltet.</span><span class="sxs-lookup"><span data-stu-id="d9898-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="d9898-130">Velg planen som du har definert begrensninger for.</span><span class="sxs-lookup"><span data-stu-id="d9898-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="d9898-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="d9898-131">Click OK.</span></span>
    * <span data-ttu-id="d9898-132">Dette kan ta en stund.</span><span class="sxs-lookup"><span data-stu-id="d9898-132">This may take a while.</span></span>  
4. <span data-ttu-id="d9898-133">Klikk Planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="d9898-133">Click Planned orders.</span></span>


