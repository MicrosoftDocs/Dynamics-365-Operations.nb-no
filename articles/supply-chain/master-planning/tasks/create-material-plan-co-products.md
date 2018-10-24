--- 
title: Opprette en materialplan for koprodukter
description: Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 2958f1e5c2e8a0cfa9cc6312f688d3b11b8e013c
ms.contentlocale: nb-no
ms.lasthandoff: 10/16/2018

---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="beddc-103">Opprette en materialplan for koprodukter</span><span class="sxs-lookup"><span data-stu-id="beddc-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="beddc-104">Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel.</span><span class="sxs-lookup"><span data-stu-id="beddc-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="beddc-105">Demonstrasjonsdatafirmaet USP2 brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="beddc-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="beddc-106">Opprett behov for et koprodukt</span><span class="sxs-lookup"><span data-stu-id="beddc-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="beddc-107">Gå til standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="beddc-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="beddc-108">Klikk Salgsordrebehandling og -spørring.</span><span class="sxs-lookup"><span data-stu-id="beddc-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="beddc-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="beddc-109">Click New.</span></span>
4. <span data-ttu-id="beddc-110">Klikk Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="beddc-110">Click Sales order.</span></span>
5. <span data-ttu-id="beddc-111">Angi en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="beddc-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="beddc-112">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="beddc-112">Example: US-001</span></span>  
6. <span data-ttu-id="beddc-113">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="beddc-113">Click OK.</span></span>
7. <span data-ttu-id="beddc-114">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="beddc-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="beddc-115">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="beddc-115">Example: P6003</span></span>  
8. <span data-ttu-id="beddc-116">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="beddc-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="beddc-117">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="beddc-117">Example: 50000</span></span>  
9. <span data-ttu-id="beddc-118">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="beddc-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="beddc-119">Opprette en materialplan for koprodukter</span><span class="sxs-lookup"><span data-stu-id="beddc-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="beddc-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="beddc-120">Close the page.</span></span>
2. <span data-ttu-id="beddc-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="beddc-121">Close the page.</span></span>
3. <span data-ttu-id="beddc-122">Klikk Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="beddc-122">Click Master planning.</span></span>
4. <span data-ttu-id="beddc-123">Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="beddc-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="beddc-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="beddc-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="beddc-125">Eksempel: Hovedplan</span><span class="sxs-lookup"><span data-stu-id="beddc-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="beddc-126">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="beddc-126">Click Run.</span></span>
7. <span data-ttu-id="beddc-127">Vis eller skjul delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="beddc-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="beddc-128">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="beddc-128">Click Filter.</span></span>
9. <span data-ttu-id="beddc-129">I listen merker du raden for felt = varenummer.</span><span class="sxs-lookup"><span data-stu-id="beddc-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="beddc-130">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="beddc-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="beddc-131">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="beddc-131">Example: P6003</span></span>  
11. <span data-ttu-id="beddc-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="beddc-132">Click OK.</span></span>
12. <span data-ttu-id="beddc-133">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="beddc-133">Click OK.</span></span>
13. <span data-ttu-id="beddc-134">Klikk Planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="beddc-134">Click Planned orders.</span></span>
14. <span data-ttu-id="beddc-135">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="beddc-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="beddc-136">Du kan for eksempel filtrere på Varenummer-feltet med verdien P6000.</span><span class="sxs-lookup"><span data-stu-id="beddc-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="beddc-137">Filtrer etter formelvaren som har som koprodukt for varen som du har opprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="beddc-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="beddc-138">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="beddc-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="beddc-139">Velg en av radene som returneres av filteret.</span><span class="sxs-lookup"><span data-stu-id="beddc-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="beddc-140">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="beddc-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="beddc-141">Vis eller skjul delen Utligning.</span><span class="sxs-lookup"><span data-stu-id="beddc-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="beddc-142">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="beddc-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="beddc-143">Den planlagte bestillingen er knyttet til salgsordren for koproduktet.</span><span class="sxs-lookup"><span data-stu-id="beddc-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="beddc-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="beddc-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="beddc-145">Opprett behov for et koprodukt</span><span class="sxs-lookup"><span data-stu-id="beddc-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="beddc-146">Gå til standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="beddc-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="beddc-147">Klikk Salgsordrebehandling og -spørring.</span><span class="sxs-lookup"><span data-stu-id="beddc-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="beddc-148">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="beddc-148">Click New.</span></span>
4. <span data-ttu-id="beddc-149">Klikk Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="beddc-149">Click Sales order.</span></span>
5. <span data-ttu-id="beddc-150">Angi en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="beddc-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="beddc-151">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="beddc-151">Example: US-001</span></span>  
6. <span data-ttu-id="beddc-152">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="beddc-152">Click OK.</span></span>
7. <span data-ttu-id="beddc-153">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="beddc-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="beddc-154">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="beddc-154">Example: P6003</span></span>  
8. <span data-ttu-id="beddc-155">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="beddc-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="beddc-156">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="beddc-156">Example: 50000</span></span>  
9. <span data-ttu-id="beddc-157">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="beddc-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="beddc-158">Opprette en materialplan for koprodukter</span><span class="sxs-lookup"><span data-stu-id="beddc-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="beddc-159">Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="beddc-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="beddc-160">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="beddc-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="beddc-161">Eksempel: Hovedplan</span><span class="sxs-lookup"><span data-stu-id="beddc-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="beddc-162">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="beddc-162">Click Run.</span></span>
4. <span data-ttu-id="beddc-163">Vis eller skjul delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="beddc-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="beddc-164">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="beddc-164">Click Filter.</span></span>
6. <span data-ttu-id="beddc-165">I listen merker du raden for felt = varenummer.</span><span class="sxs-lookup"><span data-stu-id="beddc-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="beddc-166">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="beddc-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="beddc-167">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="beddc-167">Example: P6003</span></span>  
8. <span data-ttu-id="beddc-168">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="beddc-168">Click OK.</span></span>
9. <span data-ttu-id="beddc-169">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="beddc-169">Click OK.</span></span>
10. <span data-ttu-id="beddc-170">Klikk Planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="beddc-170">Click Planned orders.</span></span>
11. <span data-ttu-id="beddc-171">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="beddc-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="beddc-172">Du kan for eksempel filtrere på Varenummer-feltet med verdien P6000.</span><span class="sxs-lookup"><span data-stu-id="beddc-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="beddc-173">Filtrer etter formelvaren som har som koprodukt for varen som du har opprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="beddc-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="beddc-174">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="beddc-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="beddc-175">Velg en av radene som returneres av filteret.</span><span class="sxs-lookup"><span data-stu-id="beddc-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="beddc-176">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="beddc-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="beddc-177">Vis eller skjul delen Utligning.</span><span class="sxs-lookup"><span data-stu-id="beddc-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="beddc-178">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="beddc-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="beddc-179">Den planlagte bestillingen er knyttet til salgsordren for koproduktet.</span><span class="sxs-lookup"><span data-stu-id="beddc-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="beddc-180">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="beddc-180">Close the page.</span></span>
17. <span data-ttu-id="beddc-181">Klikk Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="beddc-181">Click Master planning.</span></span>
18. <span data-ttu-id="beddc-182">Gå til Hovedplanlegging > Oppsett > Parametere for hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="beddc-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="beddc-183">Velg Nei i feltet Deaktiver alle planleggingsprosesser.</span><span class="sxs-lookup"><span data-stu-id="beddc-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="beddc-184">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="beddc-184">Close the page.</span></span>


