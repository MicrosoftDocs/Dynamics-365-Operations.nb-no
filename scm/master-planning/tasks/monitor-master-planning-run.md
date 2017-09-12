--- 
title: "Overvåke en kjøring av hovedplanlegging"
description: "Produksjonsplanleggeren vil se om det er en kjøring for hovedplanlegging pågår."
author: YuyuScheller
manager: AnnBe
ms.date: 06/10/2016
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
ms.openlocfilehash: 1e08d9fd3388561563e6fb982416186a652b4ce2
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="01299-103">Overvåke en kjøring av hovedplanlegging</span><span class="sxs-lookup"><span data-stu-id="01299-103">Monitor a master planning run</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="01299-104">Produksjonsplanleggeren vil se om det er en kjøring for hovedplanlegging pågår.</span><span class="sxs-lookup"><span data-stu-id="01299-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="01299-105">Bruk USMF-demodatafirmaet til å utføre denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="01299-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="01299-106">Kjør hovedplanlegging</span><span class="sxs-lookup"><span data-stu-id="01299-106">Run master planning</span></span>
1. <span data-ttu-id="01299-107">Klikk Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="01299-107">Click Master planning.</span></span>
    * <span data-ttu-id="01299-108">Du finner dette på standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="01299-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="01299-109">Angi eller velg en verdi i Plan-feltet.</span><span class="sxs-lookup"><span data-stu-id="01299-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="01299-110">Eksempel: Statisk plan</span><span class="sxs-lookup"><span data-stu-id="01299-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="01299-111">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="01299-111">Click Run.</span></span>
4. <span data-ttu-id="01299-112">Velg Ja i feltet Spor behandlingstid.</span><span class="sxs-lookup"><span data-stu-id="01299-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="01299-113">Hvis feltet allerede er valgt, hopper du over trinnet.</span><span class="sxs-lookup"><span data-stu-id="01299-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="01299-114">Angi et tall i feltet Antall tråder.</span><span class="sxs-lookup"><span data-stu-id="01299-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="01299-115">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="01299-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="01299-116">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="01299-116">Click Filter.</span></span>
8. <span data-ttu-id="01299-117">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="01299-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="01299-118">Merk raden der Felt = Varenummer.</span><span class="sxs-lookup"><span data-stu-id="01299-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="01299-119">Angi eller velg en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="01299-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="01299-120">Eksempel: T0001</span><span class="sxs-lookup"><span data-stu-id="01299-120">Example: T0001</span></span>  
10. <span data-ttu-id="01299-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="01299-121">Click OK.</span></span>
11. <span data-ttu-id="01299-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="01299-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="01299-123">Overvåke kjøringen av hovedplanlegging</span><span class="sxs-lookup"><span data-stu-id="01299-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="01299-124">Klikk Logg.</span><span class="sxs-lookup"><span data-stu-id="01299-124">Click History.</span></span>
2. <span data-ttu-id="01299-125">Klikk Forespørsler.</span><span class="sxs-lookup"><span data-stu-id="01299-125">Click Inquiries.</span></span>
3. <span data-ttu-id="01299-126">Klikk Varighet for prosessoppgave.</span><span class="sxs-lookup"><span data-stu-id="01299-126">Click Process task duration.</span></span>
4. <span data-ttu-id="01299-127">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="01299-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="01299-128">Du kan få en oversikt over hvor lang tid det tok for å fullføre hvert planleggingstrinn for hver vare.</span><span class="sxs-lookup"><span data-stu-id="01299-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  


