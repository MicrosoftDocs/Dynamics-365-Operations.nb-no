---
title: Overvåke en kjøring av hovedplanlegging
description: Produksjonsplanleggeren vil se om det er en kjøring for hovedplanlegging pågår.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, InventItemIdLookupSimple, ReqLog, ReqProcessTaskTrace
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b923b215528ecceaed9b5057ddb736ec959f1d65
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1845119"
---
# <a name="monitor-a-master-planning-run"></a><span data-ttu-id="e26c5-103">Overvåke en kjøring av hovedplanlegging</span><span class="sxs-lookup"><span data-stu-id="e26c5-103">Monitor a master planning run</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="e26c5-104">Produksjonsplanleggeren vil se om det er en kjøring for hovedplanlegging pågår.</span><span class="sxs-lookup"><span data-stu-id="e26c5-104">The production planner wants to see if a master planning run is in progress.</span></span> <span data-ttu-id="e26c5-105">Bruk USMF-demodatafirmaet til å utføre denne prosedyren.</span><span class="sxs-lookup"><span data-stu-id="e26c5-105">Use the demo data company USMF to complete this procedure.</span></span>


## <a name="run-master-planning"></a><span data-ttu-id="e26c5-106">Kjør hovedplanlegging</span><span class="sxs-lookup"><span data-stu-id="e26c5-106">Run master planning</span></span>
1. <span data-ttu-id="e26c5-107">Klikk Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="e26c5-107">Click Master planning.</span></span>
    * <span data-ttu-id="e26c5-108">Du finner dette på standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="e26c5-108">You'll find this on the default dashboard.</span></span>  
2. <span data-ttu-id="e26c5-109">Angi eller velg en verdi i Plan-feltet.</span><span class="sxs-lookup"><span data-stu-id="e26c5-109">In the Plan field, enter or select a value.</span></span>
    * <span data-ttu-id="e26c5-110">Eksempel: Statisk plan</span><span class="sxs-lookup"><span data-stu-id="e26c5-110">Example: StaticPlan</span></span>  
3. <span data-ttu-id="e26c5-111">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="e26c5-111">Click Run.</span></span>
4. <span data-ttu-id="e26c5-112">Velg Ja i feltet Spor behandlingstid.</span><span class="sxs-lookup"><span data-stu-id="e26c5-112">Select Yes in the Track processing time field.</span></span>
    * <span data-ttu-id="e26c5-113">Hvis feltet allerede er valgt, hopper du over trinnet.</span><span class="sxs-lookup"><span data-stu-id="e26c5-113">If the field is already selected, skip this step.</span></span>  
5. <span data-ttu-id="e26c5-114">Angi et tall i feltet Antall tråder.</span><span class="sxs-lookup"><span data-stu-id="e26c5-114">In the Number of threads field, enter a number.</span></span>
6. <span data-ttu-id="e26c5-115">Utvid delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="e26c5-115">Expand the Records to include section.</span></span>
7. <span data-ttu-id="e26c5-116">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="e26c5-116">Click Filter.</span></span>
8. <span data-ttu-id="e26c5-117">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="e26c5-117">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="e26c5-118">Merk raden der Felt = Varenummer.</span><span class="sxs-lookup"><span data-stu-id="e26c5-118">Mark the row where Field = Item number.</span></span>  
9. <span data-ttu-id="e26c5-119">Angi eller velg en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="e26c5-119">In the Criteria field, enter or select a value.</span></span>
    * <span data-ttu-id="e26c5-120">Eksempel: T0001</span><span class="sxs-lookup"><span data-stu-id="e26c5-120">Example: T0001</span></span>  
10. <span data-ttu-id="e26c5-121">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="e26c5-121">Click OK.</span></span>
11. <span data-ttu-id="e26c5-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="e26c5-122">Click OK.</span></span>

## <a name="monitor-the-master-planning-run"></a><span data-ttu-id="e26c5-123">Overvåke kjøringen av hovedplanlegging</span><span class="sxs-lookup"><span data-stu-id="e26c5-123">Monitor the master planning run</span></span>
1. <span data-ttu-id="e26c5-124">Klikk Logg.</span><span class="sxs-lookup"><span data-stu-id="e26c5-124">Click History.</span></span>
2. <span data-ttu-id="e26c5-125">Klikk Forespørsler.</span><span class="sxs-lookup"><span data-stu-id="e26c5-125">Click Inquiries.</span></span>
3. <span data-ttu-id="e26c5-126">Klikk Varighet for prosessoppgave.</span><span class="sxs-lookup"><span data-stu-id="e26c5-126">Click Process task duration.</span></span>
4. <span data-ttu-id="e26c5-127">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="e26c5-127">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="e26c5-128">Du kan få en oversikt over hvor lang tid det tok for å fullføre hvert planleggingstrinn for hver vare.</span><span class="sxs-lookup"><span data-stu-id="e26c5-128">For each item you can get an overview of how long it took to complete each planning step.</span></span>  

