---
title: Opprette en konsernintern plan
description: Denne fremgangsmåten viser hvordan du oppretter en konsernintern plan.
author: ChristianRytt
ms.date: 08/13/2019
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: ReqIntercompanyPlanningGroupSetup,  ReqCreatePlanWorkspace
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: crytt
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f8cf4ed879b6b2202d0b0f1f45052f5e21452967
ms.sourcegitcommit: 9b07d536b4bd8addfbdba42d2429c9fedb664635
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/07/2021
ms.locfileid: "5867356"
---
# <a name="create-an-intercompany-plan"></a><span data-ttu-id="683b2-103">Opprette en konsernintern plan</span><span class="sxs-lookup"><span data-stu-id="683b2-103">Create an intercompany plan</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="683b2-104">Denne fremgangsmåten viser hvordan du oppretter en konsernintern plan.</span><span class="sxs-lookup"><span data-stu-id="683b2-104">This procedure shows how to create an intercompany plan.</span></span> <span data-ttu-id="683b2-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="683b2-105">The demo data company used to create this procedure is USMF.</span></span>

## <a name="set-up-an-intercompany-planning-group"></a><span data-ttu-id="683b2-106">Konfigurere en konsernintern planleggingsgruppe</span><span class="sxs-lookup"><span data-stu-id="683b2-106">Set up an intercompany planning group</span></span>

1. <span data-ttu-id="683b2-107">I **navigasjonsruten** går du til **Moduler > Hovedplanlegging >Oppsett > Grupper for konsernintern planlegging**.</span><span class="sxs-lookup"><span data-stu-id="683b2-107">In the **Navigation pane**, go to **Modules > Master planning > Setup > Intercompany planning groups**.</span></span>
2. <span data-ttu-id="683b2-108">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="683b2-108">Use the Quick Filter to find records.</span></span> <span data-ttu-id="683b2-109">Du kan for eksempel filtrere på Navn-feltet med verdien 10.</span><span class="sxs-lookup"><span data-stu-id="683b2-109">For example, filter on the Name field with a value of '10'.</span></span>
3. <span data-ttu-id="683b2-110">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="683b2-110">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="683b2-111">Velg **Slett**.</span><span class="sxs-lookup"><span data-stu-id="683b2-111">Select **Delete**.</span></span> <span data-ttu-id="683b2-112">Dette trinnet er nødvendig for å forkorte kjøringen av den konserninterne planleggingen.</span><span class="sxs-lookup"><span data-stu-id="683b2-112">This step is necessary in order to shorten the intercompany planning run.</span></span>   <span data-ttu-id="683b2-113">Konsernintern planlegging kjører hovedplanlegging i alle selskaper i en planleggingsgruppe, fra den laveste planleggingssekvensen.</span><span class="sxs-lookup"><span data-stu-id="683b2-113">Intercompany planning will run master planning in all the companies in a planning group, starting from the lowest scheduling sequence.</span></span>  
5. <span data-ttu-id="683b2-114">Velg **Ja**.</span><span class="sxs-lookup"><span data-stu-id="683b2-114">Select **Yes**.</span></span>
6. <span data-ttu-id="683b2-115">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="683b2-115">Close the page.</span></span>

## <a name="create-an-intercompany-master-plan"></a><span data-ttu-id="683b2-116">Opprette en konsernintern hovedplan</span><span class="sxs-lookup"><span data-stu-id="683b2-116">Create an intercompany master plan</span></span>

1. <span data-ttu-id="683b2-117">I **navigasjonsruten** går du til **Moduler > Hovedplanlegging >Arbeidsområder > Hovedplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="683b2-117">In the **Navigation pane**, go to **Modules > Master planning > Workspaces > Master planning**.</span></span>
2. <span data-ttu-id="683b2-118">Velg **Konsernintern hovedplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="683b2-118">Select **Intercompany master planning**.</span></span>  
3. <span data-ttu-id="683b2-119">Velg rullegardinknappen i feltet **Konsernintern planleggingsgruppe** for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="683b2-119">In the **Intercompany planning group** field, select the drop-down button to open the lookup.</span></span>
4. <span data-ttu-id="683b2-120">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="683b2-120">In the list, select the link in the selected row.</span></span> <span data-ttu-id="683b2-121">Velg konsernintern planleggingsgruppe 10.</span><span class="sxs-lookup"><span data-stu-id="683b2-121">Select intercompany planning group 10.</span></span>  
5. <span data-ttu-id="683b2-122">Angi 2 i feltet **Antall konserninterne planleggingsgjentakelser.**.</span><span class="sxs-lookup"><span data-stu-id="683b2-122">In the **Number of intercompany planning iterations** field, enter '2'.</span></span> <span data-ttu-id="683b2-123">Konsernintern planleggingsgruppe 10 har to medlemmer.</span><span class="sxs-lookup"><span data-stu-id="683b2-123">Intercompany planning group 10 has two members.</span></span> <span data-ttu-id="683b2-124">For å overføre forsinkelsene fra kildefirmaet (USMF) til kunden (DEMF), må du kjøre konsernintern i begge firmaene to ganger.</span><span class="sxs-lookup"><span data-stu-id="683b2-124">In order to propagate the delays from the source company (USMF) to the customer company (DEMF), you will need to run intercompany in both companies two times.</span></span> <span data-ttu-id="683b2-125">Den første gjentakelsen vil overføre behovet og identifisere forsinkelsene i kildeselskapet (USMF).</span><span class="sxs-lookup"><span data-stu-id="683b2-125">The first iteration will propagate the demand and identify the delays in the source company (USMF).</span></span> <span data-ttu-id="683b2-126">Den andre gjentakelsen vil overføre forsinkelsene fra USMF til DEMF.</span><span class="sxs-lookup"><span data-stu-id="683b2-126">The second iteration will propagate the delays from USMF to DEMF.</span></span>  
6. <span data-ttu-id="683b2-127">Velg Ny generering i feltet **Første gjentakelse**.</span><span class="sxs-lookup"><span data-stu-id="683b2-127">In the **First iteration** field, select 'Regeneration'.</span></span>
7. <span data-ttu-id="683b2-128">Velg Ny generering i feltet **Etterfølgende gjentakelser**.</span><span class="sxs-lookup"><span data-stu-id="683b2-128">In the **Subsequent iterations** field, select 'Regeneration'.</span></span>
8. <span data-ttu-id="683b2-129">Angi et tall i feltet **Antall tråder**.</span><span class="sxs-lookup"><span data-stu-id="683b2-129">In the **Number of threads** field, enter a number.</span></span> <span data-ttu-id="683b2-130">Dette representerer antall parallelle tråder som brukes til planlegging.</span><span class="sxs-lookup"><span data-stu-id="683b2-130">This represents the number of parallel threads used for planning.</span></span>  
9. <span data-ttu-id="683b2-131">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="683b2-131">Select **OK**.</span></span>

## <a name="view-the-result-of-the-plan"></a><span data-ttu-id="683b2-132">Vise resultatet av planen</span><span class="sxs-lookup"><span data-stu-id="683b2-132">View the result of the plan</span></span>

1. <span data-ttu-id="683b2-133">Velg rullegardinknappen i **Plan**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="683b2-133">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="683b2-134">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="683b2-134">In the list, select the link in the selected row.</span></span> <span data-ttu-id="683b2-135">Velg koblingen for StaticPlan.</span><span class="sxs-lookup"><span data-stu-id="683b2-135">Select the link for StaticPlan.</span></span> <span data-ttu-id="683b2-136">Du må være i selskapet USMF.</span><span class="sxs-lookup"><span data-stu-id="683b2-136">You need to be in company USMF.</span></span>  
3. <span data-ttu-id="683b2-137">Velg **Planlagte ordrer**.</span><span class="sxs-lookup"><span data-stu-id="683b2-137">Select **Planned orders**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]