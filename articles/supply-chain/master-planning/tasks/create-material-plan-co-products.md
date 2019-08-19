---
title: Opprette en materialplan for koprodukter
description: Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: e59ff769685677b0970dbc7d4c9d4d2c1e5b63d1
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1835964"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="7f6c8-103">Opprette en materialplan for koprodukter</span><span class="sxs-lookup"><span data-stu-id="7f6c8-103">Create a material plan for co products</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7f6c8-104">Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="7f6c8-105">Demonstrasjonsdatafirmaet USP2 brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="7f6c8-106">Opprett behov for et koprodukt</span><span class="sxs-lookup"><span data-stu-id="7f6c8-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="7f6c8-107">Gå til standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="7f6c8-108">Klikk Salgsordrebehandling og -spørring.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="7f6c8-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-109">Click New.</span></span>
4. <span data-ttu-id="7f6c8-110">Klikk Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-110">Click Sales order.</span></span>
5. <span data-ttu-id="7f6c8-111">Angi en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="7f6c8-112">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="7f6c8-112">Example: US-001</span></span>  
6. <span data-ttu-id="7f6c8-113">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-113">Click OK.</span></span>
7. <span data-ttu-id="7f6c8-114">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7f6c8-115">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="7f6c8-115">Example: P6003</span></span>  
8. <span data-ttu-id="7f6c8-116">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="7f6c8-117">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="7f6c8-117">Example: 50000</span></span>  
9. <span data-ttu-id="7f6c8-118">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="7f6c8-119">Opprette en materialplan for koprodukter</span><span class="sxs-lookup"><span data-stu-id="7f6c8-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="7f6c8-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-120">Close the page.</span></span>
2. <span data-ttu-id="7f6c8-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-121">Close the page.</span></span>
3. <span data-ttu-id="7f6c8-122">Klikk Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-122">Click Master planning.</span></span>
4. <span data-ttu-id="7f6c8-123">Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="7f6c8-124">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f6c8-125">Eksempel: Hovedplan</span><span class="sxs-lookup"><span data-stu-id="7f6c8-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="7f6c8-126">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-126">Click Run.</span></span>
7. <span data-ttu-id="7f6c8-127">Vis eller skjul delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="7f6c8-128">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-128">Click Filter.</span></span>
9. <span data-ttu-id="7f6c8-129">I listen merker du raden for felt = varenummer.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="7f6c8-130">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="7f6c8-131">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="7f6c8-131">Example: P6003</span></span>  
11. <span data-ttu-id="7f6c8-132">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-132">Click OK.</span></span>
12. <span data-ttu-id="7f6c8-133">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-133">Click OK.</span></span>
13. <span data-ttu-id="7f6c8-134">Klikk Planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-134">Click Planned orders.</span></span>
14. <span data-ttu-id="7f6c8-135">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="7f6c8-136">Du kan for eksempel filtrere på Varenummer-feltet med verdien P6000.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="7f6c8-137">Filtrer etter formelvaren som har som koprodukt for varen som du har opprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="7f6c8-138">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7f6c8-139">Velg en av radene som returneres av filteret.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="7f6c8-140">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="7f6c8-141">Vis eller skjul delen Utligning.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="7f6c8-142">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f6c8-143">Den planlagte bestillingen er knyttet til salgsordren for koproduktet.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="7f6c8-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="7f6c8-145">Opprett behov for et koprodukt</span><span class="sxs-lookup"><span data-stu-id="7f6c8-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="7f6c8-146">Gå til standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="7f6c8-147">Klikk Salgsordrebehandling og -spørring.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="7f6c8-148">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-148">Click New.</span></span>
4. <span data-ttu-id="7f6c8-149">Klikk Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-149">Click Sales order.</span></span>
5. <span data-ttu-id="7f6c8-150">Angi en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="7f6c8-151">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="7f6c8-151">Example: US-001</span></span>  
6. <span data-ttu-id="7f6c8-152">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-152">Click OK.</span></span>
7. <span data-ttu-id="7f6c8-153">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="7f6c8-154">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="7f6c8-154">Example: P6003</span></span>  
8. <span data-ttu-id="7f6c8-155">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="7f6c8-156">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="7f6c8-156">Example: 50000</span></span>  
9. <span data-ttu-id="7f6c8-157">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="7f6c8-158">Opprette en materialplan for koprodukter</span><span class="sxs-lookup"><span data-stu-id="7f6c8-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="7f6c8-159">Klikk rullegardinknappen i Plan-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="7f6c8-160">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f6c8-161">Eksempel: Hovedplan</span><span class="sxs-lookup"><span data-stu-id="7f6c8-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="7f6c8-162">Klikk Kjør.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-162">Click Run.</span></span>
4. <span data-ttu-id="7f6c8-163">Vis eller skjul delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="7f6c8-164">Klikk Filter.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-164">Click Filter.</span></span>
6. <span data-ttu-id="7f6c8-165">I listen merker du raden for felt = varenummer.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="7f6c8-166">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="7f6c8-167">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="7f6c8-167">Example: P6003</span></span>  
8. <span data-ttu-id="7f6c8-168">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-168">Click OK.</span></span>
9. <span data-ttu-id="7f6c8-169">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-169">Click OK.</span></span>
10. <span data-ttu-id="7f6c8-170">Klikk Planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-170">Click Planned orders.</span></span>
11. <span data-ttu-id="7f6c8-171">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="7f6c8-172">Du kan for eksempel filtrere på Varenummer-feltet med verdien P6000.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="7f6c8-173">Filtrer etter formelvaren som har som koprodukt for varen som du har opprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="7f6c8-174">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="7f6c8-175">Velg en av radene som returneres av filteret.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="7f6c8-176">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="7f6c8-177">Vis eller skjul delen Utligning.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="7f6c8-178">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7f6c8-179">Den planlagte bestillingen er knyttet til salgsordren for koproduktet.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="7f6c8-180">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-180">Close the page.</span></span>
17. <span data-ttu-id="7f6c8-181">Klikk Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-181">Click Master planning.</span></span>
18. <span data-ttu-id="7f6c8-182">Gå til Hovedplanlegging > Oppsett > Parametere for hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="7f6c8-183">Velg Nei i feltet Deaktiver alle planleggingsprosesser.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="7f6c8-184">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7f6c8-184">Close the page.</span></span>

