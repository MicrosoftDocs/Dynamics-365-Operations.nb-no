---
title: Opprette en konsernintern plan
description: Denne fremgangsmåten viser hvordan du oppretter en konsernintern plan.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: d378a89bbb4de6d67db0019dc72a27945d50c4e9
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "333743"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="3f8d4-103">Opprette en konsernintern plan</span><span class="sxs-lookup"><span data-stu-id="3f8d4-103">Create an intercompany plan</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="3f8d4-104">Denne fremgangsmåten viser hvordan du oppretter en konsernintern plan.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="3f8d4-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="3f8d4-106">Konfigurere en konsernintern planleggingsgruppe</span><span class="sxs-lookup"><span data-stu-id="3f8d4-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="3f8d4-107">Gå til konserninterne planleggingsgrupper.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-107">Go to Intercompany planning groups.</span></span>
    * <span data-ttu-id="3f8d4-108">Hovedplanlegging > Oppsett > Konserninterne planleggingsgrupper</span><span class="sxs-lookup"><span data-stu-id="3f8d4-108">Master planning > Setup > Intercompany planning groups</span></span>  
2. <span data-ttu-id="3f8d4-109">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-109">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3f8d4-110">Du kan for eksempel filtrere på Navn-feltet med verdien 10.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-110">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="3f8d4-111">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-111">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="3f8d4-112">Klikk Slett.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-112">Click Delete.</span></span>
    * <span data-ttu-id="3f8d4-113">Dette trinnet er nødvendig for å forkorte kjøringen av den konserninterne planleggingen.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-113">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="3f8d4-114">Konsernintern planlegging kjører hovedplanlegging i alle selskaper i en planleggingsgruppe, fra den laveste planleggingssekvensen.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-114">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="3f8d4-115">Klikk Ja.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-115">Click Yes.</span></span>
6. <span data-ttu-id="3f8d4-116">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-116">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="3f8d4-117">Opprette en konsernintern plan</span><span class="sxs-lookup"><span data-stu-id="3f8d4-117">Create an intercompany plan</span></span>
1. <span data-ttu-id="3f8d4-118">Klikk Konsernintern hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-118">Click Intercompany master planning.</span></span>
    * <span data-ttu-id="3f8d4-119">Dette er i Hovedplanlegging-arbeidsområdet.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-119">This is on the Master planning workspace.</span></span>  
2. <span data-ttu-id="3f8d4-120">Klikk rullegardinknappen i feltet Konsernintern planleggingsgruppe for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-120">In the Intercompany planning group field, click the drop-down button to open the lookup.</span></span>
3. <span data-ttu-id="3f8d4-121">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-121">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3f8d4-122">Velg konsernintern planleggingsgruppe 10.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-122">Select intercompany planning group 10.</span></span>  
4. <span data-ttu-id="3f8d4-123">Angi 2 i feltet Antall konserninterne planleggingsgjentakelser.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-123">In the Number of intercompany planning iterations field, enter '2'.</span></span>
    * <span data-ttu-id="3f8d4-124">Konsernintern planleggingsgruppe 10 har to medlemmer.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-124">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="3f8d4-125">For å overføre forsinkelsene fra kildefirmaet (USMF) til kunden (DEMF), må du kjøre konsernintern i begge firmaene to ganger.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-125">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="3f8d4-126">Den første gjentakelsen vil overføre behovet og identifisere forsinkelsene i kildeselskapet (USMF).</span><span class="sxs-lookup"><span data-stu-id="3f8d4-126">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="3f8d4-127">Den andre gjentakelsen vil overføre forsinkelsene fra USMF til DEMF.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-127">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
5. <span data-ttu-id="3f8d4-128">Velg et alternativ i feltet Første gjentakelse.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-128">In the First iteration field, select an option.</span></span>
6. <span data-ttu-id="3f8d4-129">Velg Ny generering i feltet Første gjentakelse.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-129">In the First iteration field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="3f8d4-130">Velg Ny generering i feltet Etterfølgende gjentakelser.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-130">In the Subsequent iterations field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="3f8d4-131">Angi et tall i feltet Antall tråder.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-131">In the Number of threads field, enter a number.</span></span>
    * <span data-ttu-id="3f8d4-132">Dette representerer antall parallelle tråder som brukes til planlegging.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-132">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="3f8d4-133">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-133">Click OK.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="3f8d4-134">Vise resultatet av planen</span><span class="sxs-lookup"><span data-stu-id="3f8d4-134">View the result of the plan</span></span>
1. <span data-ttu-id="3f8d4-135">Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-135">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="3f8d4-136">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-136">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="3f8d4-137">Klikk koblingen for StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-137">Click the link for StaticPlan.</span></span> <span data-ttu-id="3f8d4-138">Du må være i selskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-138">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="3f8d4-139">Klikk Planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="3f8d4-139">Click Planned orders.</span></span>

