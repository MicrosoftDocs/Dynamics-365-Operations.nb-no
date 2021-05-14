---
title: Opprette en materialplan for koprodukter
description: Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, SalesOrderProcessingWorkspace, SalesCreateOrder, SalesTable, ReqCreatePlanWorkspace, ReqTransPlanCard, SysQueryForm, ReqTransPo
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: b51e4b4d00da2babb5128d8c4c22139b0c1853d4
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5920735"
---
# <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="ed146-103">Opprette en materialplan for koprodukter</span><span class="sxs-lookup"><span data-stu-id="ed146-103">Create a material plan for co products</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="ed146-104">Produksjonsplanleggeren planlegger materialbehovet for varer som er koprodukter for formel.</span><span class="sxs-lookup"><span data-stu-id="ed146-104">The production planner plans the material requirements for items that are formula co-products.</span></span> <span data-ttu-id="ed146-105">Demonstrasjonsdatafirmaet USP2 brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="ed146-105">The demo data company used to create this procedure is USP2.</span></span>

## <a name="create-requirement-for-a-co-product"></a><span data-ttu-id="ed146-106">Opprett behov for et koprodukt</span><span class="sxs-lookup"><span data-stu-id="ed146-106">Create requirement for a co-product</span></span>

1. <span data-ttu-id="ed146-107">Gå til **Salg og markedsføring \> Arbeidsområder \> Salgsordrebehandling og -spørring**.</span><span class="sxs-lookup"><span data-stu-id="ed146-107">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="ed146-108">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ed146-108">Select **New**.</span></span>
1. <span data-ttu-id="ed146-109">Velg **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="ed146-109">Select **Sales order**.</span></span>
1. <span data-ttu-id="ed146-110">Skriv inn en verdi i **Kundekonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ed146-110">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="ed146-111">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="ed146-111">Example: US-001</span></span>  
1. <span data-ttu-id="ed146-112">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed146-112">Select **OK**.</span></span>
1. <span data-ttu-id="ed146-113">Skriv inn en verdi i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ed146-113">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="ed146-114">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="ed146-114">Example: P6003</span></span>  
1. <span data-ttu-id="ed146-115">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ed146-115">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="ed146-116">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="ed146-116">Example: 50000</span></span>  
1. <span data-ttu-id="ed146-117">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ed146-117">Select **Save**.</span></span>

## <a name="create-a-material-plan-for-co-products"></a><span data-ttu-id="ed146-118">Opprette en materialplan for koprodukter</span><span class="sxs-lookup"><span data-stu-id="ed146-118">Create a material plan for co-products</span></span>

1. <span data-ttu-id="ed146-119">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ed146-119">Close the page.</span></span>
1. <span data-ttu-id="ed146-120">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ed146-120">Close the page.</span></span>
1. <span data-ttu-id="ed146-121">Velg **Hovedplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="ed146-121">Select **Master planning**.</span></span>
1. <span data-ttu-id="ed146-122">Velg rullegardinknappen i **Plan**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ed146-122">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
1. <span data-ttu-id="ed146-123">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ed146-123">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="ed146-124">Eksempel: Hovedplan</span><span class="sxs-lookup"><span data-stu-id="ed146-124">Example: MasterPlan</span></span>  
1. <span data-ttu-id="ed146-125">Velg **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="ed146-125">Select **Run**.</span></span>
1. <span data-ttu-id="ed146-126">Vis eller skjul delen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="ed146-126">Expand or collapse the **Records to include** section.</span></span>
1. <span data-ttu-id="ed146-127">Velg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="ed146-127">Select **Filter**.</span></span>
1. <span data-ttu-id="ed146-128">I listen merker du raden for **Felt** = *Varenummer*.</span><span class="sxs-lookup"><span data-stu-id="ed146-128">In the list, select the row for **Field** = *Item number*.</span></span>
1. <span data-ttu-id="ed146-129">Skriv inn en verdi i **Kriterier**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ed146-129">In the **Criteria** field, type a value.</span></span>
    * <span data-ttu-id="ed146-130">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="ed146-130">Example: P6003</span></span>  
1. <span data-ttu-id="ed146-131">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed146-131">Select **OK**.</span></span>
1. <span data-ttu-id="ed146-132">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed146-132">Select **OK**.</span></span>
1. <span data-ttu-id="ed146-133">Velg **Planlagte ordrer**.</span><span class="sxs-lookup"><span data-stu-id="ed146-133">Select **Planned orders**.</span></span>
1. <span data-ttu-id="ed146-134">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="ed146-134">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ed146-135">Du kan for eksempel filtrere på **Varenummer**-feltet med verdien P6000.</span><span class="sxs-lookup"><span data-stu-id="ed146-135">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="ed146-136">Filtrer etter formelvaren som har som koprodukt for varen som du har opprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="ed146-136">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
1. <span data-ttu-id="ed146-137">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ed146-137">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ed146-138">Velg en av radene som returneres av filteret.</span><span class="sxs-lookup"><span data-stu-id="ed146-138">Select any of the rows returned by the filter.</span></span>  
1. <span data-ttu-id="ed146-139">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ed146-139">In the list, select the link in the selected row.</span></span>
1. <span data-ttu-id="ed146-140">Vis **Utligning**-delen.</span><span class="sxs-lookup"><span data-stu-id="ed146-140">Expand the **Pegging** section.</span></span>
1. <span data-ttu-id="ed146-141">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ed146-141">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="ed146-142">Den planlagte bestillingen er knyttet til salgsordren for koproduktet.</span><span class="sxs-lookup"><span data-stu-id="ed146-142">The planned order is pegged to the sales order for the co-product.</span></span>  
1. <span data-ttu-id="ed146-143">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ed146-143">Close the page.</span></span>

## <a name="create-a-second-requirement-for-a-co-product"></a><span data-ttu-id="ed146-144">Opprette et nytt behov for et koprodukt</span><span class="sxs-lookup"><span data-stu-id="ed146-144">Create a second requirement for a co-product</span></span>

1. <span data-ttu-id="ed146-145">Gå til **Salg og markedsføring \> Arbeidsområder \> Salgsordrebehandling og -spørring**.</span><span class="sxs-lookup"><span data-stu-id="ed146-145">Go to **Sales and marketing \> Workspaces \> Sales order processing and inquiry**.</span></span>
1. <span data-ttu-id="ed146-146">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="ed146-146">Select **New**.</span></span>
1. <span data-ttu-id="ed146-147">Velg **Salgsordre**.</span><span class="sxs-lookup"><span data-stu-id="ed146-147">Select **Sales order**.</span></span>
1. <span data-ttu-id="ed146-148">Skriv inn en verdi i **Kundekonto**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ed146-148">In the **Customer account** field, type a value.</span></span>
    * <span data-ttu-id="ed146-149">Eksempel: US-001</span><span class="sxs-lookup"><span data-stu-id="ed146-149">Example: US-001</span></span>  
1. <span data-ttu-id="ed146-150">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed146-150">Select **OK**.</span></span>
1. <span data-ttu-id="ed146-151">Skriv inn en verdi i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ed146-151">In the **Item number** field, type a value.</span></span>
    * <span data-ttu-id="ed146-152">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="ed146-152">Example: P6003</span></span>  
1. <span data-ttu-id="ed146-153">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="ed146-153">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="ed146-154">Eksempel: 50000</span><span class="sxs-lookup"><span data-stu-id="ed146-154">Example: 50000</span></span>  
1. <span data-ttu-id="ed146-155">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="ed146-155">Select **Save**.</span></span>

## <a name="create-a-second-material-plan-for-co-products"></a><span data-ttu-id="ed146-156">Opprette en ny materialplan for koprodukter</span><span class="sxs-lookup"><span data-stu-id="ed146-156">Create a second material plan for co-products</span></span>

1. <span data-ttu-id="ed146-157">Velg rullegardinknappen i **Plan**-feltet for å åpne oppslaget.</span><span class="sxs-lookup"><span data-stu-id="ed146-157">In the **Plan** field, select the drop-down button to open the lookup.</span></span>
2. <span data-ttu-id="ed146-158">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ed146-158">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="ed146-159">Eksempel: Hovedplan</span><span class="sxs-lookup"><span data-stu-id="ed146-159">Example: MasterPlan</span></span>  
3. <span data-ttu-id="ed146-160">Velg **Kjør**.</span><span class="sxs-lookup"><span data-stu-id="ed146-160">Select **Run**.</span></span>
4. <span data-ttu-id="ed146-161">Vis eller skjul delen **Poster som skal inkluderes**.</span><span class="sxs-lookup"><span data-stu-id="ed146-161">Expand or collapse the **Records to include** section.</span></span>
5. <span data-ttu-id="ed146-162">Velg **Filter**.</span><span class="sxs-lookup"><span data-stu-id="ed146-162">Select **Filter**.</span></span>
6. <span data-ttu-id="ed146-163">I listen merker du raden for **Felt** = *Varenummer*.</span><span class="sxs-lookup"><span data-stu-id="ed146-163">In the list, select the row for **Field** = *Item number*.</span></span>
7. <span data-ttu-id="ed146-164">Skriv inn en verdi i *Kriterier*-feltet.</span><span class="sxs-lookup"><span data-stu-id="ed146-164">In the *Criteria* field, type a value.</span></span>
    * <span data-ttu-id="ed146-165">Eksempel: P6003</span><span class="sxs-lookup"><span data-stu-id="ed146-165">Example: P6003</span></span>  
8. <span data-ttu-id="ed146-166">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed146-166">Select **OK**.</span></span>
9. <span data-ttu-id="ed146-167">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="ed146-167">Select **OK**.</span></span>
10. <span data-ttu-id="ed146-168">Velg **Planlagte ordrer**.</span><span class="sxs-lookup"><span data-stu-id="ed146-168">Select **Planned orders**.</span></span>
11. <span data-ttu-id="ed146-169">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="ed146-169">Use the Quick Filter to find records.</span></span> <span data-ttu-id="ed146-170">Du kan for eksempel filtrere på **Varenummer**-feltet med verdien P6000.</span><span class="sxs-lookup"><span data-stu-id="ed146-170">For example, filter on the **Item number** field with a value of 'P6000'.</span></span>
    * <span data-ttu-id="ed146-171">Filtrer etter formelvaren som har som koprodukt for varen som du har opprettet en salgsordre for.</span><span class="sxs-lookup"><span data-stu-id="ed146-171">Filter by the formula item that has as co-product of the item that you created a sales order for.</span></span>  
12. <span data-ttu-id="ed146-172">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ed146-172">In the list, mark the selected row.</span></span>
    * <span data-ttu-id="ed146-173">Velg en av radene som returneres av filteret.</span><span class="sxs-lookup"><span data-stu-id="ed146-173">Select any of the rows returned by the filter.</span></span>  
13. <span data-ttu-id="ed146-174">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ed146-174">In the list, select the link in the selected row.</span></span>
14. <span data-ttu-id="ed146-175">Vis eller skjul delen **Utligning**.</span><span class="sxs-lookup"><span data-stu-id="ed146-175">Expand or collapse the **Pegging** section.</span></span>
15. <span data-ttu-id="ed146-176">Velg koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="ed146-176">In the list, select the link in the selected row.</span></span>
    * <span data-ttu-id="ed146-177">Den planlagte bestillingen er knyttet til salgsordren for koproduktet.</span><span class="sxs-lookup"><span data-stu-id="ed146-177">The planned order is pegged to the sales order for the co-product.</span></span>  
16. <span data-ttu-id="ed146-178">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ed146-178">Close the page.</span></span>
17. <span data-ttu-id="ed146-179">Velg **Hovedplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="ed146-179">Select **Master planning**.</span></span>
18. <span data-ttu-id="ed146-180">Gå til **Hovedplanlegging \> Oppsett \> Parametere for hovedplanlegging**.</span><span class="sxs-lookup"><span data-stu-id="ed146-180">Go to **Master planning \> Setup \> Master planning parameters**.</span></span>
19. <span data-ttu-id="ed146-181">Velg *Nei* i feltet **Deaktiver alle planleggingsprosesser**.</span><span class="sxs-lookup"><span data-stu-id="ed146-181">Select *No* in the **Disable all planning processes** field.</span></span>
20. <span data-ttu-id="ed146-182">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="ed146-182">Close the page.</span></span>


[!INCLUDE[footer-include](../../../includes/footer-banner.md)]