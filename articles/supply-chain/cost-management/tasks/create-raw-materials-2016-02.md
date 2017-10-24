--- 
title: "Opprette råvarer (bare februar 2016)"
description: "Denne oppgaven fokuserer på å opprette komponentene i ferdige produkter og halvfabrikata."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: YuyuScheller
ms.search.scope: Operations
ms.search.region: Global
ms.author: bis
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 3d77dcc20fe7402af83dd724e7fef848977e5bf8
ms.openlocfilehash: f6af7b93d8d1d9a6f7474f24177b16e5295e90d6
ms.contentlocale: nb-no
ms.lasthandoff: 09/29/2017

---
# <a name="create-raw-materials-february-2016-only"></a><span data-ttu-id="f63c3-103">Opprette råvarer (bare februar 2016)</span><span class="sxs-lookup"><span data-stu-id="f63c3-103">Create raw materials (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f63c3-104">Denne oppgaven fokuserer på å opprette komponentene i ferdige produkter og halvfabrikata.</span><span class="sxs-lookup"><span data-stu-id="f63c3-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="f63c3-105">Det er den trede oppgaven i serien stykklisteberegning.</span><span class="sxs-lookup"><span data-stu-id="f63c3-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="f63c3-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="f63c3-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="f63c3-107">Opprette det første materialet</span><span class="sxs-lookup"><span data-stu-id="f63c3-107">Create the first material</span></span>
1. <span data-ttu-id="f63c3-108">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="f63c3-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="f63c3-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f63c3-109">Click New.</span></span>
3. <span data-ttu-id="f63c3-110">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="f63c3-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f63c3-111">I dette eksemplet angir du ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="f63c3-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="f63c3-112">Angi eller velg en verdi i Varemodellgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-113">Velg STD.</span><span class="sxs-lookup"><span data-stu-id="f63c3-113">Select STD.</span></span> <span data-ttu-id="f63c3-114">STD står for standardkostnad, og er den mest brukte modellen når du arbeider med kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="f63c3-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="f63c3-115">Angi eller velg en verdi i Varegruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-116">Velg for eksempel Lyd.</span><span class="sxs-lookup"><span data-stu-id="f63c3-116">For example, select Audio.</span></span> <span data-ttu-id="f63c3-117">Dette har ingen innvirkning på kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="f63c3-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="f63c3-118">Angi eller velg en verdi i lagringsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-119">Velg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="f63c3-119">Select SiteWH.</span></span> <span data-ttu-id="f63c3-120">Bare Område og Lager blir brukt for demonstrasjon.</span><span class="sxs-lookup"><span data-stu-id="f63c3-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="f63c3-121">Angi eller velg en verdi i sporingsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-122">Sporingsdimensjoner vil ikke bli brukt i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="f63c3-123">Velg Ingen.</span><span class="sxs-lookup"><span data-stu-id="f63c3-123">Select None.</span></span>  
8. <span data-ttu-id="f63c3-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f63c3-124">Click OK.</span></span>
9. <span data-ttu-id="f63c3-125">Klikk Administrer lager i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f63c3-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="f63c3-126">Klikk Standard ordreinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="f63c3-126">Click Default order settings.</span></span>
11. <span data-ttu-id="f63c3-127">Angi eller velg en verdi i feltet Innkjøpssite.</span><span class="sxs-lookup"><span data-stu-id="f63c3-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-128">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="f63c3-129">Angi eller velg en verdi i feltet Lagersite.</span><span class="sxs-lookup"><span data-stu-id="f63c3-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-130">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f63c3-131">Angi eller velg en verdi i feltet Salgssite.</span><span class="sxs-lookup"><span data-stu-id="f63c3-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-132">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="f63c3-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f63c3-133">Close the page.</span></span>
15. <span data-ttu-id="f63c3-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f63c3-134">Close the page.</span></span>
16. <span data-ttu-id="f63c3-135">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f63c3-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f63c3-136">Klikk ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="f63c3-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="f63c3-137">Vis delen Styr kostnader.</span><span class="sxs-lookup"><span data-stu-id="f63c3-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="f63c3-138">Skriv inn en verdi i Kostgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="f63c3-139">I dette eksemplet skriver du inn M2.</span><span class="sxs-lookup"><span data-stu-id="f63c3-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="f63c3-140">Klikk Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f63c3-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="f63c3-141">Klikk Varepris.</span><span class="sxs-lookup"><span data-stu-id="f63c3-141">Click Item price.</span></span>
21. <span data-ttu-id="f63c3-142">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f63c3-142">Click New.</span></span>
22. <span data-ttu-id="f63c3-143">Angi eller velg en verdi i Versjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-144">I dette eksemplet velger du 10, som er standard etterkalkuleringstype for kostnad.</span><span class="sxs-lookup"><span data-stu-id="f63c3-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="f63c3-145">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-146">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="f63c3-147">Angi et tall i Pris-feltet</span><span class="sxs-lookup"><span data-stu-id="f63c3-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="f63c3-148">I dette eksemplet skriver du inn 10.</span><span class="sxs-lookup"><span data-stu-id="f63c3-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="f63c3-149">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f63c3-149">Click Save.</span></span>
26. <span data-ttu-id="f63c3-150">Klikk Aktiver ventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="f63c3-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="f63c3-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f63c3-151">Close the page.</span></span>
28. <span data-ttu-id="f63c3-152">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f63c3-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="f63c3-153">Opprette det andre materialet</span><span class="sxs-lookup"><span data-stu-id="f63c3-153">Create the second material</span></span>
1. <span data-ttu-id="f63c3-154">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f63c3-154">Click New.</span></span>
2. <span data-ttu-id="f63c3-155">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="f63c3-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f63c3-156">I dette eksemplet skriver du inn ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="f63c3-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="f63c3-157">Angi eller velg en verdi i Varemodellgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-158">Velg STD.</span><span class="sxs-lookup"><span data-stu-id="f63c3-158">Select STD.</span></span> <span data-ttu-id="f63c3-159">STD står for standardkostnad, og er den mest brukte modellen når du arbeider med kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="f63c3-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="f63c3-160">Angi eller velg en verdi i Varegruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-161">Velg for eksempel Lyd.</span><span class="sxs-lookup"><span data-stu-id="f63c3-161">For example, select Audio.</span></span> <span data-ttu-id="f63c3-162">Dette har ingen innvirkning på kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="f63c3-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="f63c3-163">Angi eller velg en verdi i lagringsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-164">Velg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="f63c3-164">Select SiteWH.</span></span> <span data-ttu-id="f63c3-165">Bare Område og Lager blir brukt i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="f63c3-166">Angi eller velg en verdi i sporingsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-167">Sporingsdimensjoner vil ikke bli brukt i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="f63c3-168">Velg Ingen.</span><span class="sxs-lookup"><span data-stu-id="f63c3-168">Select None.</span></span>  
7. <span data-ttu-id="f63c3-169">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f63c3-169">Click OK.</span></span>
8. <span data-ttu-id="f63c3-170">Klikk Administrer lager i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f63c3-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="f63c3-171">Klikk Standard ordreinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="f63c3-171">Click Default order settings.</span></span>
10. <span data-ttu-id="f63c3-172">Angi eller velg en verdi i feltet Innkjøpssite.</span><span class="sxs-lookup"><span data-stu-id="f63c3-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-173">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="f63c3-174">Angi eller velg en verdi i feltet Lagersite.</span><span class="sxs-lookup"><span data-stu-id="f63c3-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-175">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="f63c3-176">Angi eller velg en verdi i feltet Salgssite.</span><span class="sxs-lookup"><span data-stu-id="f63c3-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-177">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f63c3-178">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f63c3-178">Close the page.</span></span>
14. <span data-ttu-id="f63c3-179">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f63c3-179">Close the page.</span></span>
15. <span data-ttu-id="f63c3-180">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f63c3-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f63c3-181">Klikk ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="f63c3-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="f63c3-182">Vis delen Styr kostnader.</span><span class="sxs-lookup"><span data-stu-id="f63c3-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="f63c3-183">Skriv inn en verdi i Kostgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="f63c3-184">I dette eksemplet skriver du inn M2.</span><span class="sxs-lookup"><span data-stu-id="f63c3-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="f63c3-185">Klikk Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f63c3-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="f63c3-186">Klikk Varepris.</span><span class="sxs-lookup"><span data-stu-id="f63c3-186">Click Item price.</span></span>
20. <span data-ttu-id="f63c3-187">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f63c3-187">Click New.</span></span>
21. <span data-ttu-id="f63c3-188">Angi eller velg en verdi i Versjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-189">Velg 10 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-189">For this example, select 10.</span></span> <span data-ttu-id="f63c3-190">Dette er standard etterkalkuleringstype for kostnad.</span><span class="sxs-lookup"><span data-stu-id="f63c3-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="f63c3-191">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-192">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="f63c3-193">Angi et tall i Pris-feltet</span><span class="sxs-lookup"><span data-stu-id="f63c3-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="f63c3-194">For demonstrasjonen skriver du inn 10.</span><span class="sxs-lookup"><span data-stu-id="f63c3-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="f63c3-195">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f63c3-195">Click Save.</span></span>
25. <span data-ttu-id="f63c3-196">Klikk Aktiver ventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="f63c3-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="f63c3-197">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f63c3-197">Close the page.</span></span>
27. <span data-ttu-id="f63c3-198">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f63c3-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="f63c3-199">Opprette det tredje materialet</span><span class="sxs-lookup"><span data-stu-id="f63c3-199">Create the third material</span></span>
1. <span data-ttu-id="f63c3-200">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f63c3-200">Click New.</span></span>
2. <span data-ttu-id="f63c3-201">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="f63c3-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f63c3-202">For demonstrasjonen skriver du inn ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="f63c3-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="f63c3-203">Angi eller velg en verdi i Varemodellgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-204">Velg STD.</span><span class="sxs-lookup"><span data-stu-id="f63c3-204">Select STD.</span></span> <span data-ttu-id="f63c3-205">STD står for standardkostnad, og er den mest brukte modellen når du arbeider med kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="f63c3-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="f63c3-206">Angi eller velg en verdi i Varegruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-207">Velg for eksempel Lyd.</span><span class="sxs-lookup"><span data-stu-id="f63c3-207">For example, select Audio.</span></span> <span data-ttu-id="f63c3-208">Dette har ingen innvirkning på kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="f63c3-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="f63c3-209">Angi eller velg en verdi i lagringsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-210">Velg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="f63c3-210">Select SiteWH.</span></span> <span data-ttu-id="f63c3-211">Bare Område og Lager blir brukt for demonstrasjon.</span><span class="sxs-lookup"><span data-stu-id="f63c3-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="f63c3-212">Angi eller velg en verdi i sporingsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-213">Sporingsdimensjoner vil ikke bli brukt i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="f63c3-214">Velg Ingen.</span><span class="sxs-lookup"><span data-stu-id="f63c3-214">Select None.</span></span>  
7. <span data-ttu-id="f63c3-215">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f63c3-215">Click OK.</span></span>
8. <span data-ttu-id="f63c3-216">Klikk Administrer lager i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f63c3-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="f63c3-217">Klikk Standard ordreinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="f63c3-217">Click Default order settings.</span></span>
10. <span data-ttu-id="f63c3-218">Angi eller velg en verdi i feltet Innkjøpssite.</span><span class="sxs-lookup"><span data-stu-id="f63c3-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-219">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="f63c3-220">Angi eller velg en verdi i feltet Lagersite.</span><span class="sxs-lookup"><span data-stu-id="f63c3-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-221">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="f63c3-222">Angi eller velg en verdi i feltet Salgssite.</span><span class="sxs-lookup"><span data-stu-id="f63c3-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-223">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f63c3-224">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f63c3-224">Close the page.</span></span>
14. <span data-ttu-id="f63c3-225">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f63c3-225">Close the page.</span></span>
15. <span data-ttu-id="f63c3-226">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f63c3-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="f63c3-227">Klikk ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="f63c3-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="f63c3-228">Vis delen Styr kostnader.</span><span class="sxs-lookup"><span data-stu-id="f63c3-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="f63c3-229">Skriv inn en verdi i Kostgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="f63c3-230">I dette eksemplet skriver du inn M1.</span><span class="sxs-lookup"><span data-stu-id="f63c3-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="f63c3-231">Klikk Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f63c3-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="f63c3-232">Klikk Varepris.</span><span class="sxs-lookup"><span data-stu-id="f63c3-232">Click Item price.</span></span>
20. <span data-ttu-id="f63c3-233">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f63c3-233">Click New.</span></span>
21. <span data-ttu-id="f63c3-234">Angi eller velg en verdi i Versjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-235">Velg 10 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-235">For this example, select 10.</span></span> <span data-ttu-id="f63c3-236">Dette er standard etterkalkuleringstype for kostnad.</span><span class="sxs-lookup"><span data-stu-id="f63c3-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="f63c3-237">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f63c3-238">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f63c3-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="f63c3-239">Angi et tall i Pris-feltet</span><span class="sxs-lookup"><span data-stu-id="f63c3-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="f63c3-240">I dette eksemplet skriver du inn 10.</span><span class="sxs-lookup"><span data-stu-id="f63c3-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="f63c3-241">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f63c3-241">Click Save.</span></span>
25. <span data-ttu-id="f63c3-242">Klikk Aktiver ventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="f63c3-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="f63c3-243">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f63c3-243">Close the page.</span></span>
27. <span data-ttu-id="f63c3-244">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f63c3-244">Close the page.</span></span>


