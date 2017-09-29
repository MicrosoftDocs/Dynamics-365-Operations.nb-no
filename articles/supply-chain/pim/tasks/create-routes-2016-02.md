--- 
title: Opprette ruter (bare februar 2016)
description: "Denne oppgaven fokuserer på å opprette produksjonsruter for et ferdig produkt og et halvfabrikata."
author: BibiSp
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: bis
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 2df913543d89a502aecfe7e2fe61265a8a1a121c
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-routes-february-2016-only"></a><span data-ttu-id="4d50f-103">Opprette ruter (bare februar 2016)</span><span class="sxs-lookup"><span data-stu-id="4d50f-103">Create routes (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="4d50f-104">Denne oppgaven fokuserer på å opprette produksjonsruter for et ferdig produkt og et halvfabrikata.</span><span class="sxs-lookup"><span data-stu-id="4d50f-104">This task focuses on creating the production routes for a finished product and and a semi-finished product.</span></span> <span data-ttu-id="4d50f-105">Det er den femte oppgaven i serien stykklisteberegning.</span><span class="sxs-lookup"><span data-stu-id="4d50f-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="4d50f-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="4d50f-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="4d50f-107">Opprette en rute for et halvfabrikata</span><span class="sxs-lookup"><span data-stu-id="4d50f-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="4d50f-108">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="4d50f-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="4d50f-109">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4d50f-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4d50f-110">Velg varenummeret BOM_2.</span><span class="sxs-lookup"><span data-stu-id="4d50f-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="4d50f-111">Klikk Utvikling i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4d50f-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="4d50f-112">Klikk Rute.</span><span class="sxs-lookup"><span data-stu-id="4d50f-112">Click Route.</span></span>
5. <span data-ttu-id="4d50f-113">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4d50f-113">Click New.</span></span>
6. <span data-ttu-id="4d50f-114">Klikk Rute og ruteversjon.</span><span class="sxs-lookup"><span data-stu-id="4d50f-114">Click Route and route version.</span></span>
7. <span data-ttu-id="4d50f-115">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4d50f-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4d50f-116">I dette eksemplet skriver du inn ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="4d50f-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="4d50f-117">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="4d50f-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="4d50f-118">I dette eksemplet angir eller velger du Område 1.</span><span class="sxs-lookup"><span data-stu-id="4d50f-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="4d50f-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4d50f-119">Click OK.</span></span>
10. <span data-ttu-id="4d50f-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4d50f-120">Click New.</span></span>
11. <span data-ttu-id="4d50f-121">Angi eller velg en verdi i feltet Operasjon.</span><span class="sxs-lookup"><span data-stu-id="4d50f-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="4d50f-122">I dette eksemplet velger du Samling.</span><span class="sxs-lookup"><span data-stu-id="4d50f-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="4d50f-123">Angi et tall i feltet Kjøretid.</span><span class="sxs-lookup"><span data-stu-id="4d50f-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="4d50f-124">Skriv for eksempel 1.</span><span class="sxs-lookup"><span data-stu-id="4d50f-124">For example, type 1.</span></span> <span data-ttu-id="4d50f-125">Operasjonstid inngår ofte i prisen som er beregnet for en vare.</span><span class="sxs-lookup"><span data-stu-id="4d50f-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="4d50f-126">Angi eller velg en verdi i Rutegruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="4d50f-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="4d50f-127">Velg Std. for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="4d50f-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="4d50f-128">Klikk kategorien Oppsett.</span><span class="sxs-lookup"><span data-stu-id="4d50f-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="4d50f-129">Angi eller velg en verdi i Oppsettkategori-feltet.</span><span class="sxs-lookup"><span data-stu-id="4d50f-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="4d50f-130">I dette eksemplet velger du Samling.</span><span class="sxs-lookup"><span data-stu-id="4d50f-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="4d50f-131">Klikk kategorien Tider.</span><span class="sxs-lookup"><span data-stu-id="4d50f-131">Click the Times tab.</span></span>
17. <span data-ttu-id="4d50f-132">Angi et tall i feltet Oppstillingstid.</span><span class="sxs-lookup"><span data-stu-id="4d50f-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="4d50f-133">I dette eksemplet skriver du inn 1.</span><span class="sxs-lookup"><span data-stu-id="4d50f-133">For this example, type 1.</span></span> <span data-ttu-id="4d50f-134">Oppstillingstider inngår ofte i prisen som er beregnet for en vare.</span><span class="sxs-lookup"><span data-stu-id="4d50f-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="4d50f-135">Klikk Ruteversjon i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4d50f-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="4d50f-136">Klikk Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="4d50f-136">Click Approve.</span></span>
20. <span data-ttu-id="4d50f-137">Velg Ja under Vil du også godkjenne ruten? .</span><span class="sxs-lookup"><span data-stu-id="4d50f-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="4d50f-138">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4d50f-138">Click OK.</span></span>
22. <span data-ttu-id="4d50f-139">Klikk Ruteversjon i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4d50f-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="4d50f-140">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="4d50f-140">Click Activate.</span></span>
24. <span data-ttu-id="4d50f-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4d50f-141">Close the page.</span></span>
25. <span data-ttu-id="4d50f-142">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4d50f-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="4d50f-143">Opprette en rute for et ferdig produkt</span><span class="sxs-lookup"><span data-stu-id="4d50f-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="4d50f-144">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="4d50f-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="4d50f-145">Velg varenummeret BOM_1.</span><span class="sxs-lookup"><span data-stu-id="4d50f-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="4d50f-146">Klikk Utvikling i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4d50f-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="4d50f-147">Klikk Rute.</span><span class="sxs-lookup"><span data-stu-id="4d50f-147">Click Route.</span></span>
4. <span data-ttu-id="4d50f-148">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4d50f-148">Click New.</span></span>
5. <span data-ttu-id="4d50f-149">Klikk Rute og ruteversjon.</span><span class="sxs-lookup"><span data-stu-id="4d50f-149">Click Route and route version.</span></span>
6. <span data-ttu-id="4d50f-150">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="4d50f-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="4d50f-151">I dette eksemplet skriver du inn ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="4d50f-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="4d50f-152">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="4d50f-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="4d50f-153">I dette eksemplet angir eller velger du Område 1.</span><span class="sxs-lookup"><span data-stu-id="4d50f-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="4d50f-154">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4d50f-154">Click OK.</span></span>
9. <span data-ttu-id="4d50f-155">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="4d50f-155">Click New.</span></span>
10. <span data-ttu-id="4d50f-156">Angi eller velg en verdi i feltet Operasjon.</span><span class="sxs-lookup"><span data-stu-id="4d50f-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="4d50f-157">I dette eksemplet velger du Emballasje.</span><span class="sxs-lookup"><span data-stu-id="4d50f-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="4d50f-158">Angi et tall i feltet Kjøretid.</span><span class="sxs-lookup"><span data-stu-id="4d50f-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="4d50f-159">I dette eksemplet skriver du inn 1.</span><span class="sxs-lookup"><span data-stu-id="4d50f-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="4d50f-160">Angi eller velg en verdi i Rutegruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="4d50f-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="4d50f-161">Velg Std. for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="4d50f-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="4d50f-162">Klikk kategorien Oppsett.</span><span class="sxs-lookup"><span data-stu-id="4d50f-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="4d50f-163">Angi eller velg en verdi i Oppsettkategori-feltet.</span><span class="sxs-lookup"><span data-stu-id="4d50f-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="4d50f-164">I dette eksemplet velger du Emballasje.</span><span class="sxs-lookup"><span data-stu-id="4d50f-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="4d50f-165">Klikk kategorien Tider.</span><span class="sxs-lookup"><span data-stu-id="4d50f-165">Click the Times tab.</span></span>
16. <span data-ttu-id="4d50f-166">Angi et tall i feltet Oppstillingstid.</span><span class="sxs-lookup"><span data-stu-id="4d50f-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="4d50f-167">I dette eksemplet skriver du inn 1.</span><span class="sxs-lookup"><span data-stu-id="4d50f-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="4d50f-168">Klikk Ruteversjon i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4d50f-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="4d50f-169">Klikk Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="4d50f-169">Click Approve.</span></span>
19. <span data-ttu-id="4d50f-170">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="4d50f-170">Click OK.</span></span>
20. <span data-ttu-id="4d50f-171">Klikk Ruteversjon i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="4d50f-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="4d50f-172">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="4d50f-172">Click Activate.</span></span>
22. <span data-ttu-id="4d50f-173">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4d50f-173">Close the page.</span></span>
23. <span data-ttu-id="4d50f-174">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4d50f-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="4d50f-175">Aktiver automatisk forbruk av oppstillingstid</span><span class="sxs-lookup"><span data-stu-id="4d50f-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="4d50f-176">Gå til Produksjonskontroll > Oppsett > Ruter > Rutegrupper.</span><span class="sxs-lookup"><span data-stu-id="4d50f-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="4d50f-177">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="4d50f-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="4d50f-178">Velg Std i listen.</span><span class="sxs-lookup"><span data-stu-id="4d50f-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="4d50f-179">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="4d50f-179">Click Edit.</span></span>
4. <span data-ttu-id="4d50f-180">Velg Ja i feltet Oppstillingstid.</span><span class="sxs-lookup"><span data-stu-id="4d50f-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="4d50f-181">Oppstillingstider inngår ofte i prisen som er beregnet for en vare.</span><span class="sxs-lookup"><span data-stu-id="4d50f-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="4d50f-182">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="4d50f-182">Click Save.</span></span>
6. <span data-ttu-id="4d50f-183">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="4d50f-183">Close the page.</span></span>


