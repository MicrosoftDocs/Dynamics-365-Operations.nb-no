---
title: Opprette stykklister (februar 2016)
description: Denne oppgaven fokuserer på å opprette stykklistestrukturen for et ferdig produkt og et halvfabrikata.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, BOMConsistOf, BOMTable, InventLocationIdLookup
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 6c5cfb8aae1a61d14f7a7969f688cb282530840d
ms.sourcegitcommit: 9d4c7edd0ae2053c37c7d81cdd180b16bf3a9d3b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 05/15/2019
ms.locfileid: "1568564"
---
# <a name="create-boms-february-2016"></a><span data-ttu-id="2d30c-103">Opprette stykklister (februar 2016)</span><span class="sxs-lookup"><span data-stu-id="2d30c-103">Create BOMs (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="2d30c-104">Denne oppgaven fokuserer på å opprette stykklistestrukturen for et ferdig produkt og et halvfabrikata.</span><span class="sxs-lookup"><span data-stu-id="2d30c-104">This task focuses on creating the bill of materials structure for a finished product and a semi-finished product.</span></span> <span data-ttu-id="2d30c-105">Det er den fjerde oppgaven i serien stykklisteberegning.</span><span class="sxs-lookup"><span data-stu-id="2d30c-105">It is the fourth task in the BOM calculation series.</span></span> <span data-ttu-id="2d30c-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="2d30c-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-bom-for-a-semi-finished-product"></a><span data-ttu-id="2d30c-107">Opprette stykkliste for et halvfabrikata</span><span class="sxs-lookup"><span data-stu-id="2d30c-107">Create BOM for a semi-finished product</span></span>
1. <span data-ttu-id="2d30c-108">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="2d30c-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="2d30c-109">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2d30c-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2d30c-110">Velg varenummeret BOM_2.</span><span class="sxs-lookup"><span data-stu-id="2d30c-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="2d30c-111">Klikk Utvikling i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2d30c-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="2d30c-112">Klikk Stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="2d30c-112">Click BOM versions.</span></span>
5. <span data-ttu-id="2d30c-113">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2d30c-113">Click New.</span></span>
6. <span data-ttu-id="2d30c-114">Klikk Stykkliste og stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="2d30c-114">Click BOM and BOM version.</span></span>
7. <span data-ttu-id="2d30c-115">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="2d30c-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="2d30c-116">Skriv for eksempel BOM_2.</span><span class="sxs-lookup"><span data-stu-id="2d30c-116">For example, type BOM_2.</span></span>  
8. <span data-ttu-id="2d30c-117">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="2d30c-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="2d30c-118">I dette eksemplet angir eller velger du Område 1.</span><span class="sxs-lookup"><span data-stu-id="2d30c-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="2d30c-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2d30c-119">Click OK.</span></span>
10. <span data-ttu-id="2d30c-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2d30c-120">Click New.</span></span>
11. <span data-ttu-id="2d30c-121">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="2d30c-121">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="2d30c-122">I dette eksemplet skriver du inn ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="2d30c-122">For this example, type ITEM_C.</span></span>  
12. <span data-ttu-id="2d30c-123">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="2d30c-123">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="2d30c-124">I dette eksemplet angir eller velger du 11.</span><span class="sxs-lookup"><span data-stu-id="2d30c-124">For this example, enter or select 11.</span></span>  
13. <span data-ttu-id="2d30c-125">Klikk Overskrift.</span><span class="sxs-lookup"><span data-stu-id="2d30c-125">Click Header.</span></span>
14. <span data-ttu-id="2d30c-126">Klikk Godkjenning for å godkjenne stykklister.</span><span class="sxs-lookup"><span data-stu-id="2d30c-126">Click Approval to approve bills of materials.</span></span>
15. <span data-ttu-id="2d30c-127">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2d30c-127">Click OK.</span></span>
16. <span data-ttu-id="2d30c-128">Klikk Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="2d30c-128">Click Approve.</span></span>
    * <span data-ttu-id="2d30c-129">Godkjenn-knappen er på verktøylinjen i delen Stykklisteversjoner.</span><span class="sxs-lookup"><span data-stu-id="2d30c-129">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="2d30c-130">Hvis den er usynlig, klikker du Topptekst øverst til høyre på Stykklister-siden for å vise Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="2d30c-130">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
17. <span data-ttu-id="2d30c-131">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2d30c-131">Click OK.</span></span>
18. <span data-ttu-id="2d30c-132">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="2d30c-132">Click Activate.</span></span>
19. <span data-ttu-id="2d30c-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2d30c-133">Close the page.</span></span>
20. <span data-ttu-id="2d30c-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2d30c-134">Close the page.</span></span>
21. <span data-ttu-id="2d30c-135">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2d30c-135">Close the page.</span></span>

## <a name="create-bom-for-a-finished-product"></a><span data-ttu-id="2d30c-136">Opprette stykkliste for et ferdig produkt</span><span class="sxs-lookup"><span data-stu-id="2d30c-136">Create BOM for a finished product</span></span>
1. <span data-ttu-id="2d30c-137">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2d30c-137">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="2d30c-138">Velg varenummeret BOM_1.</span><span class="sxs-lookup"><span data-stu-id="2d30c-138">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="2d30c-139">Klikk Utvikling i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="2d30c-139">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="2d30c-140">Klikk Stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="2d30c-140">Click BOM versions.</span></span>
4. <span data-ttu-id="2d30c-141">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2d30c-141">Click New.</span></span>
5. <span data-ttu-id="2d30c-142">Klikk Stykkliste og stykklisteversjon.</span><span class="sxs-lookup"><span data-stu-id="2d30c-142">Click BOM and BOM version.</span></span>
6. <span data-ttu-id="2d30c-143">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="2d30c-143">In the Name field, type a value.</span></span>
    * <span data-ttu-id="2d30c-144">Skriv for eksempel BOM_1.</span><span class="sxs-lookup"><span data-stu-id="2d30c-144">For example, type BOM_1.</span></span>  
7. <span data-ttu-id="2d30c-145">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="2d30c-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="2d30c-146">I dette eksemplet angir eller velger du Område 1.</span><span class="sxs-lookup"><span data-stu-id="2d30c-146">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="2d30c-147">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2d30c-147">Click OK.</span></span>
9. <span data-ttu-id="2d30c-148">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2d30c-148">Click New.</span></span>
10. <span data-ttu-id="2d30c-149">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="2d30c-149">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="2d30c-150">I dette eksemplet skriver du inn ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="2d30c-150">For this example, type ITEM_A.</span></span>  
11. <span data-ttu-id="2d30c-151">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="2d30c-151">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="2d30c-152">Velg 11 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="2d30c-152">For this example, select 11.</span></span>  
12. <span data-ttu-id="2d30c-153">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2d30c-153">Click New.</span></span>
13. <span data-ttu-id="2d30c-154">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="2d30c-154">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="2d30c-155">I dette eksemplet skriver du inn ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="2d30c-155">For this example, type ITEM_B.</span></span>  
14. <span data-ttu-id="2d30c-156">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="2d30c-156">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="2d30c-157">I dette eksemplet angir eller velger du 11.</span><span class="sxs-lookup"><span data-stu-id="2d30c-157">For this example, enter or select 11.</span></span>  
15. <span data-ttu-id="2d30c-158">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="2d30c-158">Click New.</span></span>
16. <span data-ttu-id="2d30c-159">Skriv inn en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="2d30c-159">In the Item number field, type a value.</span></span>
    * <span data-ttu-id="2d30c-160">I dette eksemplet skriver du inn BOM_2.</span><span class="sxs-lookup"><span data-stu-id="2d30c-160">For this example, type BOM_2.</span></span>  
17. <span data-ttu-id="2d30c-161">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="2d30c-161">In the list, mark the selected row.</span></span>
18. <span data-ttu-id="2d30c-162">Angi eller velg en verdi i feltet Lager.</span><span class="sxs-lookup"><span data-stu-id="2d30c-162">In the Warehouse field, enter or select a value.</span></span>
    * <span data-ttu-id="2d30c-163">I dette eksemplet angir eller velger du lager 11.</span><span class="sxs-lookup"><span data-stu-id="2d30c-163">For this example, enter or select warehouse 11.</span></span>  
19. <span data-ttu-id="2d30c-164">Klikk Overskrift.</span><span class="sxs-lookup"><span data-stu-id="2d30c-164">Click Header.</span></span>
20. <span data-ttu-id="2d30c-165">Klikk Godkjenning for å godkjenne stykklister.</span><span class="sxs-lookup"><span data-stu-id="2d30c-165">Click Approval to approve bills of materials.</span></span>
21. <span data-ttu-id="2d30c-166">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2d30c-166">Click OK.</span></span>
22. <span data-ttu-id="2d30c-167">Klikk Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="2d30c-167">Click Approve.</span></span>
    * <span data-ttu-id="2d30c-168">Godkjenn-knappen er på verktøylinjen i delen Stykklisteversjoner.</span><span class="sxs-lookup"><span data-stu-id="2d30c-168">The Approve button is on the ToolBar in the  BOM versions section.</span></span> <span data-ttu-id="2d30c-169">Hvis den er usynlig, klikker du Topptekst øverst til høyre på Stykklister-siden for å vise Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="2d30c-169">If it is invisible, click Header at the upper right of the Bills of materials page to display Approve.</span></span>  
23. <span data-ttu-id="2d30c-170">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="2d30c-170">Click OK.</span></span>
24. <span data-ttu-id="2d30c-171">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="2d30c-171">Click Activate.</span></span>
25. <span data-ttu-id="2d30c-172">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2d30c-172">Close the page.</span></span>
26. <span data-ttu-id="2d30c-173">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2d30c-173">Close the page.</span></span>
27. <span data-ttu-id="2d30c-174">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="2d30c-174">Close the page.</span></span>

