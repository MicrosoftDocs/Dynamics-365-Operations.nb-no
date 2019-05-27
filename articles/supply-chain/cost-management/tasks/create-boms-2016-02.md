---
title: Opprette stykklister (bare februar 2016)
description: Denne oppgaven fokuserer på å opprette stykklistestrukturen for et ferdig produkt og et halvfabrikata.
author: ShylaThompson
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
audience: Application User
ms.reviewer: josaw
ms.search.scope: Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.openlocfilehash: f132a3865b180a74d328ebc76ca29b2fc8aee85f
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1563256"
---
# <a name="create-boms-february-2016-only"></a><span data-ttu-id="179f0-103">Opprette stykklister (bare februar 2016)</span><span class="sxs-lookup"><span data-stu-id="179f0-103">Create BOMs (February 2016 only)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="179f0-104">Denne oppgaven fokuserer på å opprette stykklistestrukturen for et ferdig produkt og et halvfabrikata.</span><span class="sxs-lookup"><span data-stu-id="179f0-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="179f0-105">Det er den fjerde oppgaven i serien stykklisteberegning.</span><span class="sxs-lookup"><span data-stu-id="179f0-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="179f0-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="179f0-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="179f0-107">Opprette stykkliste for et halvfabrikata</span><span class="sxs-lookup"><span data-stu-id="179f0-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="179f0-108">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="179f0-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="179f0-109">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="179f0-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="179f0-110">Velg varenummeret BOM_2.</span><span class="sxs-lookup"><span data-stu-id="179f0-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="179f0-111">Klikk Utvikling i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="179f0-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="179f0-112">Klikk Stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="179f0-112">Click BOM versions.</span></span>
5. <span data-ttu-id="179f0-113">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="179f0-113">Click New.</span></span>
6. <span data-ttu-id="179f0-114">Klikk Stykkliste og stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="179f0-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="179f0-115">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="179f0-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="179f0-116">Skriv for eksempel BOM_2.</span><span class="sxs-lookup"><span data-stu-id="179f0-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="179f0-117">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="179f0-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="179f0-118">I dette eksemplet angir eller velger du Område 1.</span><span class="sxs-lookup"><span data-stu-id="179f0-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="179f0-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="179f0-119">Click OK.</span></span>
10. <span data-ttu-id="179f0-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="179f0-120">Click New.</span></span>
11. <span data-ttu-id="179f0-121">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="179f0-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="179f0-122">I dette eksemplet skriver du inn ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="179f0-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="179f0-123">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="179f0-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="179f0-124">I dette eksemplet angir eller velger du 11.</span><span class="sxs-lookup"><span data-stu-id="179f0-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="179f0-125">Klikk Overskrift.</span><span class="sxs-lookup"><span data-stu-id="179f0-125">Click Header.</span></span>
14. <span data-ttu-id="179f0-126">Klikk Godkjenning for å godkjenne stykklister.</span><span class="sxs-lookup"><span data-stu-id="179f0-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="179f0-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="179f0-127">Click OK.</span></span>
16. <span data-ttu-id="179f0-128">Klikk Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="179f0-128">Click Approve.</span></span>
    * <span data-ttu-id="179f0-129">Godkjenn-knappen er på verktøylinjen i delen Stykklisteversjoner.</span><span class="sxs-lookup"><span data-stu-id="179f0-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="179f0-130">Hvis den er usynlig, klikker du Topptekst øverst til høyre på Stykklister-siden for å vise Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="179f0-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="179f0-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="179f0-131">Click OK.</span></span>
18. <span data-ttu-id="179f0-132">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="179f0-132">Click Activate.</span></span>
19. <span data-ttu-id="179f0-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="179f0-133">Close the page.</span></span>
20. <span data-ttu-id="179f0-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="179f0-134">Close the page.</span></span>
21. <span data-ttu-id="179f0-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="179f0-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="179f0-136">Opprette stykkliste for et ferdig produkt</span><span class="sxs-lookup"><span data-stu-id="179f0-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="179f0-137">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="179f0-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="179f0-138">Velg varenummeret BOM_1.</span><span class="sxs-lookup"><span data-stu-id="179f0-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="179f0-139">Klikk Utvikling i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="179f0-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="179f0-140">Klikk Stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="179f0-140">Click BOM versions.</span></span>
4. <span data-ttu-id="179f0-141">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="179f0-141">Click New.</span></span>
5. <span data-ttu-id="179f0-142">Klikk Stykkliste og stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="179f0-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="179f0-143">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="179f0-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="179f0-144">Skriv for eksempel BOM_1.</span><span class="sxs-lookup"><span data-stu-id="179f0-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="179f0-145">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="179f0-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="179f0-146">I dette eksemplet angir eller velger du Område 1.</span><span class="sxs-lookup"><span data-stu-id="179f0-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="179f0-147">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="179f0-147">Click OK.</span></span>
9. <span data-ttu-id="179f0-148">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="179f0-148">Click New.</span></span>
10. <span data-ttu-id="179f0-149">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="179f0-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="179f0-150">I dette eksemplet skriver du inn ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="179f0-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="179f0-151">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="179f0-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="179f0-152">Velg 11 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="179f0-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="179f0-153">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="179f0-153">Click New.</span></span>
13. <span data-ttu-id="179f0-154">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="179f0-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="179f0-155">I dette eksemplet skriver du inn ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="179f0-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="179f0-156">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="179f0-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="179f0-157">I dette eksemplet angir eller velger du 11.</span><span class="sxs-lookup"><span data-stu-id="179f0-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="179f0-158">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="179f0-158">Click New.</span></span>
16. <span data-ttu-id="179f0-159">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="179f0-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="179f0-160">I dette eksemplet skriver du inn BOM_2.</span><span class="sxs-lookup"><span data-stu-id="179f0-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="179f0-161">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="179f0-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="179f0-162">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="179f0-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="179f0-163">I dette eksemplet angir eller velger du lager 11.</span><span class="sxs-lookup"><span data-stu-id="179f0-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="179f0-164">Klikk Overskrift.</span><span class="sxs-lookup"><span data-stu-id="179f0-164">Click Header.</span></span>
20. <span data-ttu-id="179f0-165">Klikk Godkjenning for å godkjenne stykklister.</span><span class="sxs-lookup"><span data-stu-id="179f0-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="179f0-166">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="179f0-166">Click OK.</span></span>
22. <span data-ttu-id="179f0-167">Klikk Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="179f0-167">Click Approve.</span></span>
    * <span data-ttu-id="179f0-168">Godkjenn-knappen er på verktøylinjen i delen Stykklisteversjoner.</span><span class="sxs-lookup"><span data-stu-id="179f0-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="179f0-169">Hvis den er usynlig, klikker du Topptekst øverst til høyre på Stykklister-siden for å vise Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="179f0-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="179f0-170">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="179f0-170">Click OK.</span></span>
24. <span data-ttu-id="179f0-171">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="179f0-171">Click Activate.</span></span>
25. <span data-ttu-id="179f0-172">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="179f0-172">Close the page.</span></span>
26. <span data-ttu-id="179f0-173">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="179f0-173">Close the page.</span></span>
27. <span data-ttu-id="179f0-174">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="179f0-174">Close the page.</span></span>

