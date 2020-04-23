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
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 3a64817f140d8a2302b3b2c2d1e55de103a5bb36
ms.sourcegitcommit: 4f9912439ff78acf0c754d5bff972c4b85763093
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/02/2020
ms.locfileid: "3209703"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="a45dd-103">Opprette en konsernintern plan</span><span class="sxs-lookup"><span data-stu-id="a45dd-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a45dd-104">Denne fremgangsmåten viser hvordan du oppretter en konsernintern plan.</span><span class="sxs-lookup"><span data-stu-id="a45dd-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="a45dd-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="a45dd-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="a45dd-106">Konfigurere en konsernintern planleggingsgruppe</span><span class="sxs-lookup"><span data-stu-id="a45dd-106">Set up an intercompany planning group</span></span> 
1. <span data-ttu-id="a45dd-107">I **navigasjonsruten** går du til **Moduler > Hovedplanlegging >Oppsett > Grupper for konsernintern planlegging**.</span><span class="sxs-lookup"><span data-stu-id="a45dd-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span> 
2. <span data-ttu-id="a45dd-108">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="a45dd-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="a45dd-109">Du kan for eksempel filtrere på Navn-feltet med verdien 10.</span><span class="sxs-lookup"><span data-stu-id="a45dd-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="a45dd-110">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a45dd-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a45dd-111">Klikk **Slett**.</span><span class="sxs-lookup"><span data-stu-id="a45dd-111">Click **Delete**.</span></span> <span data-ttu-id="a45dd-112">Dette trinnet er nødvendig for å forkorte kjøringen av den konserninterne planleggingen.</span><span class="sxs-lookup"><span data-stu-id="a45dd-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="a45dd-113">Konsernintern planlegging kjører hovedplanlegging i alle selskaper i en planleggingsgruppe, fra den laveste planleggingssekvensen.</span><span class="sxs-lookup"><span data-stu-id="a45dd-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="a45dd-114">Klikk **Ja**.</span><span class="sxs-lookup"><span data-stu-id="a45dd-114">Click **Yes**.</span></span>
6. <span data-ttu-id="a45dd-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="a45dd-115">Close the page.</span></span>

## <a name="create-an-intercompany-plan"></a><span data-ttu-id="a45dd-116">Opprette en konsernintern plan</span><span class="sxs-lookup"><span data-stu-id="a45dd-116">Create an intercompany plan</span></span>
1. <span data-ttu-id="a45dd-117">I **navigasjonsruten** går du til **Moduler > Hovedplanlegging >Arbeidsområder > Hovedplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="a45dd-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="a45dd-118">Klikk **Konsernintern hovedplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="a45dd-118">Click **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="a45dd-119">Klikk rullegardinknappen i feltet **Konsernintern planleggingsgruppe** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="a45dd-119">In the **Intercompany planning group** field, click the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="a45dd-120">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a45dd-120">In the list, click the link in the selected row.</span></span> <span data-ttu-id="a45dd-121">Velg konsernintern planleggingsgruppe 10.</span><span class="sxs-lookup"><span data-stu-id="a45dd-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="a45dd-122">Angi 2 i feltet **Antall konserninterne planleggingsgjentakelser.**.</span><span class="sxs-lookup"><span data-stu-id="a45dd-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="a45dd-123">Konsernintern planleggingsgruppe 10 har to medlemmer.</span><span class="sxs-lookup"><span data-stu-id="a45dd-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="a45dd-124">For å overføre forsinkelsene fra kildefirmaet (USMF) til kunden (DEMF), må du kjøre konsernintern i begge firmaene to ganger.</span><span class="sxs-lookup"><span data-stu-id="a45dd-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="a45dd-125">Den første gjentakelsen vil overføre behovet og identifisere forsinkelsene i kildeselskapet (USMF).</span><span class="sxs-lookup"><span data-stu-id="a45dd-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="a45dd-126">Den andre gjentakelsen vil overføre forsinkelsene fra USMF til DEMF.</span><span class="sxs-lookup"><span data-stu-id="a45dd-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="a45dd-127">Velg Ny generering i feltet **Første gjentakelse**.</span><span class="sxs-lookup"><span data-stu-id="a45dd-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="a45dd-128">Velg Ny generering i feltet **Etterfølgende gjentakelser**.</span><span class="sxs-lookup"><span data-stu-id="a45dd-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="a45dd-129">Angi et tall i feltet **Antall tråder**.</span><span class="sxs-lookup"><span data-stu-id="a45dd-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="a45dd-130">Dette representerer antall parallelle tråder som brukes til planlegging.</span><span class="sxs-lookup"><span data-stu-id="a45dd-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="a45dd-131">Klikk **OK**.</span><span class="sxs-lookup"><span data-stu-id="a45dd-131">Click **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="a45dd-132">Vise resultatet av planen</span><span class="sxs-lookup"><span data-stu-id="a45dd-132">View the result of the plan</span></span>
1. <span data-ttu-id="a45dd-133">Klikk rullegardinknappen i **Plan**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="a45dd-133">In the **Plan** field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="a45dd-134">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a45dd-134">In the list, click the link in the selected row.</span></span> <span data-ttu-id="a45dd-135">Klikk koblingen for StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="a45dd-135">Click the link for StaticPlan.</span></span> <span data-ttu-id="a45dd-136">Du må være i selskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="a45dd-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="a45dd-137">Klikk **Planlagte bestillinger**.</span><span class="sxs-lookup"><span data-stu-id="a45dd-137">Click **Planned orders**.</span></span>

