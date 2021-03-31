---
title: Opprette en materialplan for koprodukter
description: Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2a87935f8f30d909f1a6a62ed7be00c83476a36a
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5214376"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="da157-103">Opprette en materialplan for koprodukter</span><span class="sxs-lookup"><span data-stu-id="da157-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="da157-104">Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel.</span><span class="sxs-lookup"><span data-stu-id="da157-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="da157-105">Demonstrasjonsdatafirmaet USP2 brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="da157-105">The demo data company used to create this procedure is USP2.</span></span>


## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="da157-106">Opprett behov for et koprodukt</span><span class="sxs-lookup"><span data-stu-id="da157-106">Create requirement for a co-product</span></span>
1. <span data-ttu-id="da157-107">Gå til standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="da157-107">Go to Default dashboard.</span></span>
2. <span data-ttu-id="da157-108">Klikk på Salgsordrebehandling og -spørring.</span><span class="sxs-lookup"><span data-stu-id="da157-108">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="da157-109">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="da157-109">Click New.</span></span>
4. <span data-ttu-id="da157-110">Klikk på Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="da157-110">Click Sales order.</span></span>
5. <span data-ttu-id="da157-111">Angi en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="da157-111">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="da157-112">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="da157-112">Example: US-001</span></span>  
6. <span data-ttu-id="da157-113">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="da157-113">Click OK.</span></span>
7. <span data-ttu-id="da157-114">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="da157-114">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="da157-115">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="da157-115">Example: P6003</span></span>  
8. <span data-ttu-id="da157-116">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="da157-116">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="da157-117">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="da157-117">Example: 50000</span></span>  
9. <span data-ttu-id="da157-118">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="da157-118">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="da157-119">Opprette en materialplan for koprodukter</span><span class="sxs-lookup"><span data-stu-id="da157-119">Create a material plan for co-products</span></span>
1. <span data-ttu-id="da157-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="da157-120">Close the page.</span></span>
2. <span data-ttu-id="da157-121">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="da157-121">Close the page.</span></span>
3. <span data-ttu-id="da157-122">Klikk på Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="da157-122">Click Master planning.</span></span>
4. <span data-ttu-id="da157-123">Klikk på rullegardinknappen i Plan-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="da157-123">In the Plan field, click the drop-down button to open the lookup.</span></span>
5. <span data-ttu-id="da157-124">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="da157-124">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="da157-125">Eksempel: Hovedplan</span><span class="sxs-lookup"><span data-stu-id="da157-125">Example: MasterPlan</span></span>  
6. <span data-ttu-id="da157-126">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="da157-126">Click Run.</span></span>
7. <span data-ttu-id="da157-127">Vis eller skjul delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="da157-127">Expand or collapse the Records to include section.</span></span>
8. <span data-ttu-id="da157-128">Klikk på Filter.</span><span class="sxs-lookup"><span data-stu-id="da157-128">Click Filter.</span></span>
9. <span data-ttu-id="da157-129">I listen merker du raden for felt = varenummer.</span><span class="sxs-lookup"><span data-stu-id="da157-129">In the list, select the row for Field = Item number.</span></span>
10. <span data-ttu-id="da157-130">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="da157-130">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="da157-131">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="da157-131">Example: P6003</span></span>  
11. <span data-ttu-id="da157-132">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="da157-132">Click OK.</span></span>
12. <span data-ttu-id="da157-133">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="da157-133">Click OK.</span></span>
13. <span data-ttu-id="da157-134">Klikk på Planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="da157-134">Click Planned orders.</span></span>
14. <span data-ttu-id="da157-135">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="da157-135">Use the Quick Filter to find records.</span></span> <span data-ttu-id="da157-136">Du kan for eksempel filtrere på Varenummer-feltet med verdien P6000.</span><span class="sxs-lookup"><span data-stu-id="da157-136">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="da157-137">Filtrer etter formelvaren som har som koprodukt for varen som du har opprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="da157-137">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
15. <span data-ttu-id="da157-138">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="da157-138">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="da157-139">Velg en av radene som returneres av filteret.</span><span class="sxs-lookup"><span data-stu-id="da157-139">Select any of the rows returned by the filter.</span></span>  
16. <span data-ttu-id="da157-140">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="da157-140">In the list, click the link in the selected row.</span></span>
17. <span data-ttu-id="da157-141">Vis eller skjul delen Utligning.</span><span class="sxs-lookup"><span data-stu-id="da157-141">Expand or collapse the Pegging section.</span></span>
18. <span data-ttu-id="da157-142">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="da157-142">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="da157-143">Den planlagte bestillingen er knyttet til salgsordren for koproduktet.</span><span class="sxs-lookup"><span data-stu-id="da157-143">The planned order is pegged to the sales order for the co-product.</span></span>  
19. <span data-ttu-id="da157-144">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="da157-144">Close the page.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="da157-145">Opprett behov for et koprodukt</span><span class="sxs-lookup"><span data-stu-id="da157-145">Create requirement for a co-product</span></span>
1. <span data-ttu-id="da157-146">Gå til standard instrumentbord.</span><span class="sxs-lookup"><span data-stu-id="da157-146">Go to Default dashboard.</span></span>
2. <span data-ttu-id="da157-147">Klikk på Salgsordrebehandling og -spørring.</span><span class="sxs-lookup"><span data-stu-id="da157-147">Click Sales order processing and inquiry.</span></span>
3. <span data-ttu-id="da157-148">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="da157-148">Click New.</span></span>
4. <span data-ttu-id="da157-149">Klikk på Salgsordre.</span><span class="sxs-lookup"><span data-stu-id="da157-149">Click Sales order.</span></span>
5. <span data-ttu-id="da157-150">Angi en verdi i Kundekonto-feltet.</span><span class="sxs-lookup"><span data-stu-id="da157-150">In the Customer account field, type a value.</span></span>
    * <span data-ttu-id="da157-151">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="da157-151">Example: US-001</span></span>  
6. <span data-ttu-id="da157-152">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="da157-152">Click OK.</span></span>
7. <span data-ttu-id="da157-153">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="da157-153">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="da157-154">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="da157-154">Example: P6003</span></span>  
8. <span data-ttu-id="da157-155">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="da157-155">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="da157-156">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="da157-156">Example: 50000</span></span>  
9. <span data-ttu-id="da157-157">Klikk på Lagre.</span><span class="sxs-lookup"><span data-stu-id="da157-157">Click Save.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="da157-158">Opprette en materialplan for koprodukter</span><span class="sxs-lookup"><span data-stu-id="da157-158">Create a material plan for co-products</span></span>
1. <span data-ttu-id="da157-159">Klikk på rullegardinknappen i Plan-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="da157-159">In the Plan field, click the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="da157-160">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="da157-160">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="da157-161">Eksempel: Hovedplan</span><span class="sxs-lookup"><span data-stu-id="da157-161">Example: MasterPlan</span></span>  
3. <span data-ttu-id="da157-162">Klikk på Kjør.</span><span class="sxs-lookup"><span data-stu-id="da157-162">Click Run.</span></span>
4. <span data-ttu-id="da157-163">Vis eller skjul delen Poster som skal inkluderes.</span><span class="sxs-lookup"><span data-stu-id="da157-163">Expand or collapse the Records to include section.</span></span>
5. <span data-ttu-id="da157-164">Klikk på Filter.</span><span class="sxs-lookup"><span data-stu-id="da157-164">Click Filter.</span></span>
6. <span data-ttu-id="da157-165">I listen merker du raden for felt = varenummer.</span><span class="sxs-lookup"><span data-stu-id="da157-165">In the list, select the row for Field = Item number.</span></span>
7. <span data-ttu-id="da157-166">Skriv inn en verdi i Kriterier-feltet.</span><span class="sxs-lookup"><span data-stu-id="da157-166">In the Criteria field, type a value.</span></span>
    * <span data-ttu-id="da157-167">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="da157-167">Example: P6003</span></span>  
8. <span data-ttu-id="da157-168">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="da157-168">Click OK.</span></span>
9. <span data-ttu-id="da157-169">Klikk på OK.</span><span class="sxs-lookup"><span data-stu-id="da157-169">Click OK.</span></span>
10. <span data-ttu-id="da157-170">Klikk på Planlagte bestillinger.</span><span class="sxs-lookup"><span data-stu-id="da157-170">Click Planned orders.</span></span>
11. <span data-ttu-id="da157-171">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="da157-171">Use the Quick Filter to find records.</span></span> <span data-ttu-id="da157-172">Du kan for eksempel filtrere på Varenummer-feltet med verdien P6000.</span><span class="sxs-lookup"><span data-stu-id="da157-172">For example, filter on the Item number field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="da157-173">Filtrer etter formelvaren som har som koprodukt for varen som du har opprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="da157-173">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="da157-174">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="da157-174">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="da157-175">Velg en av radene som returneres av filteret.</span><span class="sxs-lookup"><span data-stu-id="da157-175">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="da157-176">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="da157-176">In the list, click the link in the selected row.</span></span>
14. <span data-ttu-id="da157-177">Vis eller skjul delen Utligning.</span><span class="sxs-lookup"><span data-stu-id="da157-177">Expand or collapse the Pegging section.</span></span>
15. <span data-ttu-id="da157-178">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="da157-178">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="da157-179">Den planlagte bestillingen er knyttet til salgsordren for koproduktet.</span><span class="sxs-lookup"><span data-stu-id="da157-179">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="da157-180">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="da157-180">Close the page.</span></span>
17. <span data-ttu-id="da157-181">Klikk på Hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="da157-181">Click Master planning.</span></span>
18. <span data-ttu-id="da157-182">Gå til Hovedplanlegging > Oppsett > Parametere for hovedplanlegging.</span><span class="sxs-lookup"><span data-stu-id="da157-182">Go to Master planning > Setup > Master planning parameters.</span></span>
19. <span data-ttu-id="da157-183">Velg Nei i feltet Deaktiver alle planleggingsprosesser.</span><span class="sxs-lookup"><span data-stu-id="da157-183">Select No in the Disable all planning processes field.</span></span>
20. <span data-ttu-id="da157-184">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="da157-184">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]