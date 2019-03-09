---
title: Opprette råvarer (februar 2016)
description: Denne oppgaven fokuserer på å opprette komponentene i ferdige produkter og halvfabrikata.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, EcoResProductCreate, InventItemOrderSetup, InventItemPrice
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 091b6edaf43e86e6e3665bf79871648473e284c7
ms.sourcegitcommit: 0f530e5f72a40f383868957a6b5cb0e446e4c795
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 01/29/2019
ms.locfileid: "351062"
---
# <a name="create-raw-materials-february-2016"></a><span data-ttu-id="7a6dc-103">Opprette råvarer (februar 2016)</span><span class="sxs-lookup"><span data-stu-id="7a6dc-103">Create raw materials (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="7a6dc-104">Denne oppgaven fokuserer på å opprette komponentene i ferdige produkter og halvfabrikata.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-104">This task focuses on creating the components of finished and semi-finished products.</span></span> <span data-ttu-id="7a6dc-105">Det er den trede oppgaven i serien stykklisteberegning.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-105">It is the third task in the BOM calculation series.</span></span> <span data-ttu-id="7a6dc-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-the-first-material"></a><span data-ttu-id="7a6dc-107">Opprette det første materialet</span><span class="sxs-lookup"><span data-stu-id="7a6dc-107">Create the first material</span></span>
1. <span data-ttu-id="7a6dc-108">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="7a6dc-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-109">Click New.</span></span>
3. <span data-ttu-id="7a6dc-110">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-110">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7a6dc-111">I dette eksemplet angir du ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-111">For this example, enter ITEM_A.</span></span>  
4. <span data-ttu-id="7a6dc-112">Angi eller velg en verdi i Varemodellgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-112">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-113">Velg STD.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-113">Select STD.</span></span> <span data-ttu-id="7a6dc-114">STD står for standardkostnad, og er den mest brukte modellen når du arbeider med kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-114">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="7a6dc-115">Angi eller velg en verdi i Varegruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-115">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-116">Velg for eksempel Lyd.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-116">For example, select Audio.</span></span> <span data-ttu-id="7a6dc-117">Dette har ingen innvirkning på kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-117">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="7a6dc-118">Angi eller velg en verdi i lagringsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-118">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-119">Velg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-119">Select SiteWH.</span></span> <span data-ttu-id="7a6dc-120">Bare Område og Lager blir brukt for demonstrasjon.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-120">Only Site and Warehouse will be used for the demonstration.</span></span>  
7. <span data-ttu-id="7a6dc-121">Angi eller velg en verdi i sporingsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-121">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-122">Sporingsdimensjoner vil ikke bli brukt i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-122">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7a6dc-123">Velg Ingen.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-123">Select None.</span></span>  
8. <span data-ttu-id="7a6dc-124">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-124">Click OK.</span></span>
9. <span data-ttu-id="7a6dc-125">Klikk Administrer lager i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-125">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="7a6dc-126">Klikk Standard ordreinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-126">Click Default order settings.</span></span>
11. <span data-ttu-id="7a6dc-127">Angi eller velg en verdi i feltet Innkjøpssite.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-128">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-128">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7a6dc-129">Angi eller velg en verdi i feltet Lagersite.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-130">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-130">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7a6dc-131">Angi eller velg en verdi i feltet Salgssite.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-132">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-132">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="7a6dc-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-133">Close the page.</span></span>
15. <span data-ttu-id="7a6dc-134">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-134">Close the page.</span></span>
16. <span data-ttu-id="7a6dc-135">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-135">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7a6dc-136">Klikk ITEM_A.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-136">Click ITEM_A.</span></span>  
17. <span data-ttu-id="7a6dc-137">Vis delen Styr kostnader.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-137">Expand the Manage costs section.</span></span>
18. <span data-ttu-id="7a6dc-138">Skriv inn en verdi i Kostgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-138">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7a6dc-139">I dette eksemplet skriver du inn M2.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-139">For this example, type M2.</span></span>  
19. <span data-ttu-id="7a6dc-140">Klikk Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-140">On the Action Pane, click Manage costs.</span></span>
20. <span data-ttu-id="7a6dc-141">Klikk Varepris.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-141">Click Item price.</span></span>
21. <span data-ttu-id="7a6dc-142">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-142">Click New.</span></span>
22. <span data-ttu-id="7a6dc-143">Angi eller velg en verdi i Versjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-143">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-144">I dette eksemplet velger du 10, som er standard etterkalkuleringstype for kostnad.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-144">For this example, select 10, which is the Standard cost costing type.</span></span>  
23. <span data-ttu-id="7a6dc-145">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-145">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-146">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-146">For this example, select Site 1.</span></span>  
24. <span data-ttu-id="7a6dc-147">Angi et tall i Pris-feltet</span><span class="sxs-lookup"><span data-stu-id="7a6dc-147">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7a6dc-148">I dette eksemplet skriver du inn 10.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-148">For this example, type 10.</span></span>  
25. <span data-ttu-id="7a6dc-149">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-149">Click Save.</span></span>
26. <span data-ttu-id="7a6dc-150">Klikk Aktiver ventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="7a6dc-150">Click Activate pending price(s).</span></span>
27. <span data-ttu-id="7a6dc-151">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-151">Close the page.</span></span>
28. <span data-ttu-id="7a6dc-152">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-152">Close the page.</span></span>

## <a name="create-the-second-material"></a><span data-ttu-id="7a6dc-153">Opprette det andre materialet</span><span class="sxs-lookup"><span data-stu-id="7a6dc-153">Create the second material</span></span>
1. <span data-ttu-id="7a6dc-154">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-154">Click New.</span></span>
2. <span data-ttu-id="7a6dc-155">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-155">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7a6dc-156">I dette eksemplet skriver du inn ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-156">For this example, type ITEM_B.</span></span>  
3. <span data-ttu-id="7a6dc-157">Angi eller velg en verdi i Varemodellgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-157">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-158">Velg STD.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-158">Select STD.</span></span> <span data-ttu-id="7a6dc-159">STD står for standardkostnad, og er den mest brukte modellen når du arbeider med kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-159">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="7a6dc-160">Angi eller velg en verdi i Varegruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-160">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-161">Velg for eksempel Lyd.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-161">For example, select Audio.</span></span> <span data-ttu-id="7a6dc-162">Dette har ingen innvirkning på kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-162">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="7a6dc-163">Angi eller velg en verdi i lagringsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-163">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-164">Velg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-164">Select SiteWH.</span></span> <span data-ttu-id="7a6dc-165">Bare Område og Lager blir brukt i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-165">Only Site and Warehouse will be used for this example.</span></span>  
6. <span data-ttu-id="7a6dc-166">Angi eller velg en verdi i sporingsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-166">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-167">Sporingsdimensjoner vil ikke bli brukt i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-167">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7a6dc-168">Velg Ingen.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-168">Select None.</span></span>  
7. <span data-ttu-id="7a6dc-169">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-169">Click OK.</span></span>
8. <span data-ttu-id="7a6dc-170">Klikk Administrer lager i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-170">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="7a6dc-171">Klikk Standard ordreinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-171">Click Default order settings.</span></span>
10. <span data-ttu-id="7a6dc-172">Angi eller velg en verdi i feltet Innkjøpssite.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-172">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-173">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-173">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="7a6dc-174">Angi eller velg en verdi i feltet Lagersite.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-174">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-175">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-175">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7a6dc-176">Angi eller velg en verdi i feltet Salgssite.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-176">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-177">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-177">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7a6dc-178">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-178">Close the page.</span></span>
14. <span data-ttu-id="7a6dc-179">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-179">Close the page.</span></span>
15. <span data-ttu-id="7a6dc-180">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-180">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7a6dc-181">Klikk ITEM_B.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-181">Click ITEM_B.</span></span>  
16. <span data-ttu-id="7a6dc-182">Vis delen Styr kostnader.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-182">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="7a6dc-183">Skriv inn en verdi i Kostgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-183">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7a6dc-184">I dette eksemplet skriver du inn M2.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-184">For this example, type M2.</span></span>  
18. <span data-ttu-id="7a6dc-185">Klikk Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-185">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="7a6dc-186">Klikk Varepris.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-186">Click Item price.</span></span>
20. <span data-ttu-id="7a6dc-187">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-187">Click New.</span></span>
21. <span data-ttu-id="7a6dc-188">Angi eller velg en verdi i Versjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-188">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-189">Velg 10 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-189">For this example, select 10.</span></span> <span data-ttu-id="7a6dc-190">Dette er standard etterkalkuleringstype for kostnad.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-190">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="7a6dc-191">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-191">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-192">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-192">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="7a6dc-193">Angi et tall i Pris-feltet</span><span class="sxs-lookup"><span data-stu-id="7a6dc-193">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7a6dc-194">For demonstrasjonen skriver du inn 10.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-194">For the demonstration, type 10.</span></span>  
24. <span data-ttu-id="7a6dc-195">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-195">Click Save.</span></span>
25. <span data-ttu-id="7a6dc-196">Klikk Aktiver ventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="7a6dc-196">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="7a6dc-197">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-197">Close the page.</span></span>
27. <span data-ttu-id="7a6dc-198">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-198">Close the page.</span></span>

## <a name="create-the-third-material"></a><span data-ttu-id="7a6dc-199">Opprette det tredje materialet</span><span class="sxs-lookup"><span data-stu-id="7a6dc-199">Create the third material</span></span>
1. <span data-ttu-id="7a6dc-200">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-200">Click New.</span></span>
2. <span data-ttu-id="7a6dc-201">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-201">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="7a6dc-202">For demonstrasjonen skriver du inn ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-202">For the demonstration, type ITEM_C</span></span>  
3. <span data-ttu-id="7a6dc-203">Angi eller velg en verdi i Varemodellgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-203">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-204">Velg STD.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-204">Select STD.</span></span> <span data-ttu-id="7a6dc-205">STD står for standardkostnad, og er den mest brukte modellen når du arbeider med kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-205">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
4. <span data-ttu-id="7a6dc-206">Angi eller velg en verdi i Varegruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-206">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-207">Velg for eksempel Lyd.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-207">For example, select Audio.</span></span> <span data-ttu-id="7a6dc-208">Dette har ingen innvirkning på kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-208">This has no impact on cost calculations.</span></span>  
5. <span data-ttu-id="7a6dc-209">Angi eller velg en verdi i lagringsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-209">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-210">Velg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-210">Select SiteWH.</span></span> <span data-ttu-id="7a6dc-211">Bare Område og Lager blir brukt for demonstrasjon.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-211">Only Site and Warehouse will be used for the demonstration.</span></span>  
6. <span data-ttu-id="7a6dc-212">Angi eller velg en verdi i sporingsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-212">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-213">Sporingsdimensjoner vil ikke bli brukt i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-213">Tracking dimensions will not be used for this example.</span></span> <span data-ttu-id="7a6dc-214">Velg Ingen.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-214">Select None.</span></span>  
7. <span data-ttu-id="7a6dc-215">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-215">Click OK.</span></span>
8. <span data-ttu-id="7a6dc-216">Klikk Administrer lager i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-216">On the Action Pane, click Manage inventory.</span></span>
9. <span data-ttu-id="7a6dc-217">Klikk Standard ordreinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-217">Click Default order settings.</span></span>
10. <span data-ttu-id="7a6dc-218">Angi eller velg en verdi i feltet Innkjøpssite.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-218">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-219">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-219">For this example, select Site 1.</span></span>  
11. <span data-ttu-id="7a6dc-220">Angi eller velg en verdi i feltet Lagersite.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-220">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-221">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-221">For this example, select Site 1.</span></span>  
12. <span data-ttu-id="7a6dc-222">Angi eller velg en verdi i feltet Salgssite.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-222">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-223">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-223">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="7a6dc-224">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-224">Close the page.</span></span>
14. <span data-ttu-id="7a6dc-225">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-225">Close the page.</span></span>
15. <span data-ttu-id="7a6dc-226">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-226">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="7a6dc-227">Klikk ITEM_C.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-227">Click ITEM_C.</span></span>  
16. <span data-ttu-id="7a6dc-228">Vis delen Styr kostnader.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-228">Expand the Manage costs section.</span></span>
17. <span data-ttu-id="7a6dc-229">Skriv inn en verdi i Kostgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-229">In the Cost group field, type a value.</span></span>
    * <span data-ttu-id="7a6dc-230">I dette eksemplet skriver du inn M1.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-230">For this example, type M1.</span></span>  
18. <span data-ttu-id="7a6dc-231">Klikk Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-231">On the Action Pane, click Manage costs.</span></span>
19. <span data-ttu-id="7a6dc-232">Klikk Varepris.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-232">Click Item price.</span></span>
20. <span data-ttu-id="7a6dc-233">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-233">Click New.</span></span>
21. <span data-ttu-id="7a6dc-234">Angi eller velg en verdi i Versjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-234">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-235">Velg 10 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-235">For this example, select 10.</span></span> <span data-ttu-id="7a6dc-236">Dette er standard etterkalkuleringstype for kostnad.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-236">This is the Standard cost costing type.</span></span>  
22. <span data-ttu-id="7a6dc-237">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-237">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="7a6dc-238">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-238">For this example, select Site 1.</span></span>  
23. <span data-ttu-id="7a6dc-239">Angi et tall i Pris-feltet</span><span class="sxs-lookup"><span data-stu-id="7a6dc-239">In the Price field, enter a number.</span></span>
    * <span data-ttu-id="7a6dc-240">I dette eksemplet skriver du inn 10.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-240">For this example, type 10.</span></span>  
24. <span data-ttu-id="7a6dc-241">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-241">Click Save.</span></span>
25. <span data-ttu-id="7a6dc-242">Klikk Aktiver ventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="7a6dc-242">Click Activate pending price(s).</span></span>
26. <span data-ttu-id="7a6dc-243">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-243">Close the page.</span></span>
27. <span data-ttu-id="7a6dc-244">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="7a6dc-244">Close the page.</span></span>

