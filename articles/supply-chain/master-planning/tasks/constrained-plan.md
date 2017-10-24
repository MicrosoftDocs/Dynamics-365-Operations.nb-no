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
ms.sourcegitcommit: f827b4787506cfdec8b9a91c4a68f3293190158a
ms.openlocfilehash: 59c6a4a2b239b3fd6b6ddc8f06bfd007f0191f0a
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="generate-a-constrained-plan"></a><span data-ttu-id="5fea9-103">Generere en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="5fea9-103">Generate a constrained plan</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="5fea9-104">Denne fremgangsmåten viser hvordan du oppretter en plan som tar hensyn til både material- og kapasitetsbegrensninger.</span><span class="sxs-lookup"><span data-stu-id="5fea9-104">This procedure shows how to create a plan that takes into account both material and capacity constraints.</span></span> <span data-ttu-id="5fea9-105">Planen sikrer at produksjonen ikke starter før materialer er tilgjengelige og ressurser er ikke overbestilt.</span><span class="sxs-lookup"><span data-stu-id="5fea9-105">The plan ensures that manufacturing doesn't start before materials are available and resources are not overbooked.</span></span> 

<span data-ttu-id="5fea9-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="5fea9-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="5fea9-107">Denne fremgangsmåten er ment for produksjonsplanleggeren.</span><span class="sxs-lookup"><span data-stu-id="5fea9-107">This procedure is intended for the production planner.</span></span>


## <a name="set-up-a-constrained-plan"></a><span data-ttu-id="5fea9-108">Definere en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="5fea9-108">Set up a constrained plan</span></span>
1. <span data-ttu-id="5fea9-109">Klikk Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="5fea9-109">Click Master planning.</span></span>
2. <span data-ttu-id="5fea9-110">Klikk Hovedplaner.</span><span class="sxs-lookup"><span data-stu-id="5fea9-110">Click Master plans.</span></span>
3. <span data-ttu-id="5fea9-111">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="5fea9-111">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="5fea9-112">Eksempel: Statisk plan</span><span class="sxs-lookup"><span data-stu-id="5fea9-112">Example: StaticPlan</span></span>  
4. <span data-ttu-id="5fea9-113">Velg Ja i Begrenset kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="5fea9-113">Select Yes in the Finite capacity field.</span></span>
5. <span data-ttu-id="5fea9-114">Angi 30 i feltet Begrenset kapasitet.</span><span class="sxs-lookup"><span data-stu-id="5fea9-114">In the Finite capacity time fence field, enter '30'.</span></span>
6. <span data-ttu-id="5fea9-115">Utvid horisontene i dager-delen.</span><span class="sxs-lookup"><span data-stu-id="5fea9-115">Expand the Time fences in days section.</span></span>
7. <span data-ttu-id="5fea9-116">Velg Ja i Kapasitet-feltet.</span><span class="sxs-lookup"><span data-stu-id="5fea9-116">Select Yes in the Capacity field.</span></span>
8. <span data-ttu-id="5fea9-117">Angi et tall i feltet Kapasitetsplanleggingshorisont (dager).</span><span class="sxs-lookup"><span data-stu-id="5fea9-117">In the Capacity scheduling time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="5fea9-118">Eksempel: 60</span><span class="sxs-lookup"><span data-stu-id="5fea9-118">Example: 60</span></span>  
9. <span data-ttu-id="5fea9-119">Velg Ja i feltet Beregnede forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="5fea9-119">Select Yes in the Calculated delays field.</span></span>
10. <span data-ttu-id="5fea9-120">Angi et tall i feltet Beregn forsinkelseshorisont (dager).</span><span class="sxs-lookup"><span data-stu-id="5fea9-120">In the Calculate delays time fence (days) field, enter a number.</span></span>
    * <span data-ttu-id="5fea9-121">Eksempel: 60</span><span class="sxs-lookup"><span data-stu-id="5fea9-121">Example: 60</span></span>  
11. <span data-ttu-id="5fea9-122">Utvid delen Beregnede forsinkelser.</span><span class="sxs-lookup"><span data-stu-id="5fea9-122">Expand the Calculated delays section.</span></span>
12. <span data-ttu-id="5fea9-123">Velg Ja i feltet Legg til den beregnede forsinkelsen i behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5fea9-123">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
13. <span data-ttu-id="5fea9-124">Velg Ja i feltet Legg til den beregnede forsinkelsen i behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5fea9-124">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
14. <span data-ttu-id="5fea9-125">Velg Ja i feltet Legg til den beregnede forsinkelsen i behovsdatoen.</span><span class="sxs-lookup"><span data-stu-id="5fea9-125">Select Yes in the Add the calculated delay to the requirement date field.</span></span>
15. <span data-ttu-id="5fea9-126">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="5fea9-126">Close the page.</span></span>

## <a name="create-a-constrained-plan"></a><span data-ttu-id="5fea9-127">Opprette en begrenset plan</span><span class="sxs-lookup"><span data-stu-id="5fea9-127">Create a constrained plan</span></span>
1. <span data-ttu-id="5fea9-128">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="5fea9-128">Click Run.</span></span>
2. <span data-ttu-id="5fea9-129">Angi eller velg en verdi i Hovedplan-feltet.</span><span class="sxs-lookup"><span data-stu-id="5fea9-129">In the Master plan field, enter or select a value.</span></span>
    * <span data-ttu-id="5fea9-130">Velg planen som du har definert begrensninger for.</span><span class="sxs-lookup"><span data-stu-id="5fea9-130">Select the plan for which you have set up constraints.</span></span>  
3. <span data-ttu-id="5fea9-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="5fea9-131">Click OK.</span></span>
    * <span data-ttu-id="5fea9-132">Dette kan ta en stund.</span><span class="sxs-lookup"><span data-stu-id="5fea9-132">This may take a while.</span></span>  
4. <span data-ttu-id="5fea9-133">Klikk Planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="5fea9-133">Click Planned orders.</span></span>


