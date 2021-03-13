---
title: Opprette en konsernintern plan
description: Denne fremgangsmåten viser hvordan du oppretter en konsernintern plan.
author: ShylaThompson
manager: tfehr
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: c368e461860a41d0110f5aed79c2aac49c437d68
ms.sourcegitcommit: 38d40c331c8894acb7b119c5073e3088b54776c1
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/15/2021
ms.locfileid: "5011420"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="6312d-103">Opprette en konsernintern plan</span><span class="sxs-lookup"><span data-stu-id="6312d-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="6312d-104">Denne fremgangsmåten viser hvordan du oppretter en konsernintern plan.</span><span class="sxs-lookup"><span data-stu-id="6312d-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="6312d-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="6312d-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="6312d-106">Konfigurere en konsernintern planleggingsgruppe</span><span class="sxs-lookup"><span data-stu-id="6312d-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="6312d-107">I **navigasjonsruten** går du til **Moduler > Hovedplanlegging >Oppsett > Grupper for konsernintern planlegging**.</span><span class="sxs-lookup"><span data-stu-id="6312d-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="6312d-108">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="6312d-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="6312d-109">Du kan for eksempel filtrere på Navn-feltet med verdien 10.</span><span class="sxs-lookup"><span data-stu-id="6312d-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="6312d-110">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6312d-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="6312d-111">Klikk på **Slett**.</span><span class="sxs-lookup"><span data-stu-id="6312d-111">Click **Delete**.</span></span> <span data-ttu-id="6312d-112">Dette trinnet er nødvendig for å forkorte kjøringen av den konserninterne planleggingen.</span><span class="sxs-lookup"><span data-stu-id="6312d-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="6312d-113">Konsernintern planlegging kjører hovedplanlegging i alle selskaper i en planleggingsgruppe, fra den laveste planleggingssekvensen.</span><span class="sxs-lookup"><span data-stu-id="6312d-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="6312d-114">Klikk på **Ja**.</span><span class="sxs-lookup"><span data-stu-id="6312d-114">Click **Yes**.</span></span>
6. <span data-ttu-id="6312d-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="6312d-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="6312d-116">Opprette en konsernintern plan</span><span class="sxs-lookup"><span data-stu-id="6312d-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="6312d-117">I **navigasjonsruten** går du til **Moduler > Hovedplanlegging >Arbeidsområder > Hovedplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="6312d-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="6312d-118">Klikk på **Konsernintern hovedplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="6312d-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="6312d-119">Klikk på rullegardinknappen i feltet **Konsernintern planleggingsgruppe** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6312d-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="6312d-120">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6312d-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="6312d-121">Velg konsernintern planleggingsgruppe 10.</span><span class="sxs-lookup"><span data-stu-id="6312d-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="6312d-122">Angi 2 i feltet **Antall konserninterne planleggingsgjentakelser.**.</span><span class="sxs-lookup"><span data-stu-id="6312d-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="6312d-123">Konsernintern planleggingsgruppe 10 har to medlemmer.</span><span class="sxs-lookup"><span data-stu-id="6312d-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="6312d-124">For å overføre forsinkelsene fra kildefirmaet (USMF) til kunden (DEMF), må du kjøre konsernintern i begge firmaene to ganger.</span><span class="sxs-lookup"><span data-stu-id="6312d-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="6312d-125">Den første gjentakelsen vil overføre behovet og identifisere forsinkelsene i kildeselskapet (USMF).</span><span class="sxs-lookup"><span data-stu-id="6312d-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="6312d-126">Den andre gjentakelsen vil overføre forsinkelsene fra USMF til DEMF.</span><span class="sxs-lookup"><span data-stu-id="6312d-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="6312d-127">Velg Ny generering i feltet **Første gjentakelse**.</span><span class="sxs-lookup"><span data-stu-id="6312d-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="6312d-128">Velg Ny generering i feltet **Etterfølgende gjentakelser**.</span><span class="sxs-lookup"><span data-stu-id="6312d-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="6312d-129">Angi et tall i feltet **Antall tråder**.</span><span class="sxs-lookup"><span data-stu-id="6312d-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="6312d-130">Dette representerer antall parallelle tråder som brukes til planlegging.</span><span class="sxs-lookup"><span data-stu-id="6312d-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="6312d-131">Klikk på **OK**.</span><span class="sxs-lookup"><span data-stu-id="6312d-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="6312d-132">Vise resultatet av planen</span><span class="sxs-lookup"><span data-stu-id="6312d-132">View the result of the plan</span></span>
1. <span data-ttu-id="6312d-133">Klikk på rullegardinknappen i **Plan**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="6312d-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="6312d-134">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="6312d-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="6312d-135">Klikk på koblingen for StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="6312d-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="6312d-136">Du må være i selskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="6312d-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="6312d-137">Klikk på **Planlagte bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="6312d-137">Click **Planned orders**.</span></span>

