---
title: Opprette ruter (februar 2016)
description: Denne oppgaven fokuserer på å opprette produksjonsruter for et ferdig produkt og et halvfabrikata.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductDetailsExtended, RouteInventProd, RouteGroup
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 5aa7db4ed66e7201d8d480d948a4249e43febde7
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844567"
---
# <a name="create-routes-february-2016"></a><span data-ttu-id="89ceb-103">Opprette ruter (februar 2016)</span><span class="sxs-lookup"><span data-stu-id="89ceb-103">Create routes (February 2016)</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="89ceb-104">Denne oppgaven fokuserer på å opprette produksjonsruter for et ferdig produkt og et halvfabrikata.</span><span class="sxs-lookup"><span data-stu-id="89ceb-104">This task focuses on creating the production routes for a finished product and a semi-finished product.</span></span> <span data-ttu-id="89ceb-105">Det er den femte oppgaven i serien stykklisteberegning.</span><span class="sxs-lookup"><span data-stu-id="89ceb-105">It is the fifth task in the BOM calculation series.</span></span> <span data-ttu-id="89ceb-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="89ceb-106">The demo data company used to create this task is USMF.</span></span>


## <a name="create-a-route-for-a-semi-finished-product"></a><span data-ttu-id="89ceb-107">Opprette en rute for et halvfabrikata</span><span class="sxs-lookup"><span data-stu-id="89ceb-107">Create a route for a semi-finished product</span></span>
1. <span data-ttu-id="89ceb-108">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="89ceb-108">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="89ceb-109">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="89ceb-109">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="89ceb-110">Velg varenummeret BOM_2.</span><span class="sxs-lookup"><span data-stu-id="89ceb-110">Select the item number BOM_2.</span></span>  
3. <span data-ttu-id="89ceb-111">Klikk Utvikling i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="89ceb-111">On the Action Pane, click Engineer.</span></span>
4. <span data-ttu-id="89ceb-112">Klikk Rute.</span><span class="sxs-lookup"><span data-stu-id="89ceb-112">Click Route.</span></span>
5. <span data-ttu-id="89ceb-113">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="89ceb-113">Click New.</span></span>
6. <span data-ttu-id="89ceb-114">Klikk Rute og ruteversjon.</span><span class="sxs-lookup"><span data-stu-id="89ceb-114">Click Route and route version.</span></span>
7. <span data-ttu-id="89ceb-115">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="89ceb-115">In the Description field, type a value.</span></span>
    * <span data-ttu-id="89ceb-116">I dette eksemplet skriver du inn ROUTE_2.</span><span class="sxs-lookup"><span data-stu-id="89ceb-116">For example, type ROUTE_2.</span></span>  
8. <span data-ttu-id="89ceb-117">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="89ceb-117">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="89ceb-118">I dette eksemplet angir eller velger du Område 1.</span><span class="sxs-lookup"><span data-stu-id="89ceb-118">For this example, enter or select Site 1.</span></span>  
9. <span data-ttu-id="89ceb-119">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="89ceb-119">Click OK.</span></span>
10. <span data-ttu-id="89ceb-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="89ceb-120">Click New.</span></span>
11. <span data-ttu-id="89ceb-121">Angi eller velg en verdi i feltet Operasjon.</span><span class="sxs-lookup"><span data-stu-id="89ceb-121">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="89ceb-122">I dette eksemplet velger du Samling.</span><span class="sxs-lookup"><span data-stu-id="89ceb-122">For this example, select Assembly.</span></span>  
12. <span data-ttu-id="89ceb-123">Angi et tall i feltet Kjøretid.</span><span class="sxs-lookup"><span data-stu-id="89ceb-123">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="89ceb-124">Skriv for eksempel 1.</span><span class="sxs-lookup"><span data-stu-id="89ceb-124">For example, type 1.</span></span> <span data-ttu-id="89ceb-125">Operasjonstid inngår ofte i prisen som er beregnet for en vare.</span><span class="sxs-lookup"><span data-stu-id="89ceb-125">Run times are often part of the price that is calculated for an item.</span></span>  
13. <span data-ttu-id="89ceb-126">Angi eller velg en verdi i Rutegruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="89ceb-126">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="89ceb-127">Velg Std. for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="89ceb-127">For this example, select Std.</span></span>  
14. <span data-ttu-id="89ceb-128">Klikk kategorien Oppsett.</span><span class="sxs-lookup"><span data-stu-id="89ceb-128">Click the Setup tab.</span></span>
15. <span data-ttu-id="89ceb-129">Angi eller velg en verdi i Oppsettkategori-feltet.</span><span class="sxs-lookup"><span data-stu-id="89ceb-129">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="89ceb-130">I dette eksemplet velger du Samling.</span><span class="sxs-lookup"><span data-stu-id="89ceb-130">For this example, select Assembly.</span></span>  
16. <span data-ttu-id="89ceb-131">Klikk kategorien Tider.</span><span class="sxs-lookup"><span data-stu-id="89ceb-131">Click the Times tab.</span></span>
17. <span data-ttu-id="89ceb-132">Angi et tall i feltet Oppstillingstid.</span><span class="sxs-lookup"><span data-stu-id="89ceb-132">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="89ceb-133">I dette eksemplet skriver du inn 1.</span><span class="sxs-lookup"><span data-stu-id="89ceb-133">For this example, type 1.</span></span> <span data-ttu-id="89ceb-134">Oppstillingstider inngår ofte i prisen som er beregnet for en vare.</span><span class="sxs-lookup"><span data-stu-id="89ceb-134">Setup times are often part of the price that is calculated for an item.</span></span>  
18. <span data-ttu-id="89ceb-135">Klikk Ruteversjon i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="89ceb-135">On the Action Pane, click Route version.</span></span>
19. <span data-ttu-id="89ceb-136">Klikk Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="89ceb-136">Click Approve.</span></span>
20. <span data-ttu-id="89ceb-137">Velg Ja under Vil du også godkjenne ruten? .</span><span class="sxs-lookup"><span data-stu-id="89ceb-137">Select Yes in the Do you also want to approve the route? field.</span></span>
21. <span data-ttu-id="89ceb-138">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="89ceb-138">Click OK.</span></span>
22. <span data-ttu-id="89ceb-139">Klikk Ruteversjon i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="89ceb-139">On the Action Pane, click Route version.</span></span>
23. <span data-ttu-id="89ceb-140">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="89ceb-140">Click Activate.</span></span>
24. <span data-ttu-id="89ceb-141">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="89ceb-141">Close the page.</span></span>
25. <span data-ttu-id="89ceb-142">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="89ceb-142">Close the page.</span></span>

## <a name="create-a-route-for-a-finished-product"></a><span data-ttu-id="89ceb-143">Opprette en rute for et ferdig produkt</span><span class="sxs-lookup"><span data-stu-id="89ceb-143">Create a route for a finished product</span></span>
1. <span data-ttu-id="89ceb-144">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="89ceb-144">In the list, click the link in the selected row.</span></span>
    * <span data-ttu-id="89ceb-145">Velg varenummeret BOM_1.</span><span class="sxs-lookup"><span data-stu-id="89ceb-145">Select the item number BOM_1.</span></span>  
2. <span data-ttu-id="89ceb-146">Klikk Utvikling i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="89ceb-146">On the Action Pane, click Engineer.</span></span>
3. <span data-ttu-id="89ceb-147">Klikk Rute.</span><span class="sxs-lookup"><span data-stu-id="89ceb-147">Click Route.</span></span>
4. <span data-ttu-id="89ceb-148">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="89ceb-148">Click New.</span></span>
5. <span data-ttu-id="89ceb-149">Klikk Rute og ruteversjon.</span><span class="sxs-lookup"><span data-stu-id="89ceb-149">Click Route and route version.</span></span>
6. <span data-ttu-id="89ceb-150">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="89ceb-150">In the Description field, type a value.</span></span>
    * <span data-ttu-id="89ceb-151">I dette eksemplet skriver du inn ROUTE_1.</span><span class="sxs-lookup"><span data-stu-id="89ceb-151">For this example, type ROUTE_1.</span></span>  
7. <span data-ttu-id="89ceb-152">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="89ceb-152">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="89ceb-153">I dette eksemplet angir eller velger du Område 1.</span><span class="sxs-lookup"><span data-stu-id="89ceb-153">For this example, enter or select Site 1.</span></span>  
8. <span data-ttu-id="89ceb-154">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="89ceb-154">Click OK.</span></span>
9. <span data-ttu-id="89ceb-155">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="89ceb-155">Click New.</span></span>
10. <span data-ttu-id="89ceb-156">Angi eller velg en verdi i feltet Operasjon.</span><span class="sxs-lookup"><span data-stu-id="89ceb-156">In the Operation field, enter or select a value.</span></span>
    * <span data-ttu-id="89ceb-157">I dette eksemplet velger du Emballasje.</span><span class="sxs-lookup"><span data-stu-id="89ceb-157">For this example, select Packing.</span></span>  
11. <span data-ttu-id="89ceb-158">Angi et tall i feltet Kjøretid.</span><span class="sxs-lookup"><span data-stu-id="89ceb-158">In the Run time field, enter a number.</span></span>
    * <span data-ttu-id="89ceb-159">I dette eksemplet skriver du inn 1.</span><span class="sxs-lookup"><span data-stu-id="89ceb-159">For this example, type 1.</span></span>  
12. <span data-ttu-id="89ceb-160">Angi eller velg en verdi i Rutegruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="89ceb-160">In the Route group field, enter or select a value.</span></span>
    * <span data-ttu-id="89ceb-161">Velg Std. for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="89ceb-161">For this example, select Std.</span></span>  
13. <span data-ttu-id="89ceb-162">Klikk kategorien Oppsett.</span><span class="sxs-lookup"><span data-stu-id="89ceb-162">Click the Setup tab.</span></span>
14. <span data-ttu-id="89ceb-163">Angi eller velg en verdi i Oppsettkategori-feltet.</span><span class="sxs-lookup"><span data-stu-id="89ceb-163">In the Setup category field, enter or select a value.</span></span>
    * <span data-ttu-id="89ceb-164">I dette eksemplet velger du Emballasje.</span><span class="sxs-lookup"><span data-stu-id="89ceb-164">For this example, select Packing.</span></span>  
15. <span data-ttu-id="89ceb-165">Klikk kategorien Tider.</span><span class="sxs-lookup"><span data-stu-id="89ceb-165">Click the Times tab.</span></span>
16. <span data-ttu-id="89ceb-166">Angi et tall i feltet Oppstillingstid.</span><span class="sxs-lookup"><span data-stu-id="89ceb-166">In the Setup time field, enter a number.</span></span>
    * <span data-ttu-id="89ceb-167">I dette eksemplet skriver du inn 1.</span><span class="sxs-lookup"><span data-stu-id="89ceb-167">For this example, type 1.</span></span>  
17. <span data-ttu-id="89ceb-168">Klikk Ruteversjon i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="89ceb-168">On the Action Pane, click Route version.</span></span>
18. <span data-ttu-id="89ceb-169">Klikk Godkjenn.</span><span class="sxs-lookup"><span data-stu-id="89ceb-169">Click Approve.</span></span>
19. <span data-ttu-id="89ceb-170">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="89ceb-170">Click OK.</span></span>
20. <span data-ttu-id="89ceb-171">Klikk Ruteversjon i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="89ceb-171">On the Action Pane, click Route version.</span></span>
21. <span data-ttu-id="89ceb-172">Klikk Aktiver.</span><span class="sxs-lookup"><span data-stu-id="89ceb-172">Click Activate.</span></span>
22. <span data-ttu-id="89ceb-173">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="89ceb-173">Close the page.</span></span>
23. <span data-ttu-id="89ceb-174">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="89ceb-174">Close the page.</span></span>

## <a name="enable-automatic-consumption-of-setup-time"></a><span data-ttu-id="89ceb-175">Aktiver automatisk forbruk av oppstillingstid</span><span class="sxs-lookup"><span data-stu-id="89ceb-175">Enable automatic consumption of setup time</span></span>
1. <span data-ttu-id="89ceb-176">Gå til Produksjonskontroll > Oppsett > Ruter > Rutegrupper.</span><span class="sxs-lookup"><span data-stu-id="89ceb-176">Go to Production control > Setup > Routes > Route groups.</span></span>
2. <span data-ttu-id="89ceb-177">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="89ceb-177">In the list, find and select the desired record.</span></span>
    * <span data-ttu-id="89ceb-178">Velg Std i listen.</span><span class="sxs-lookup"><span data-stu-id="89ceb-178">Select Std in the list.</span></span>  
3. <span data-ttu-id="89ceb-179">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="89ceb-179">Click Edit.</span></span>
4. <span data-ttu-id="89ceb-180">Velg Ja i feltet Oppstillingstid.</span><span class="sxs-lookup"><span data-stu-id="89ceb-180">Select Yes in the Setup time field.</span></span>
    * <span data-ttu-id="89ceb-181">Oppstillingstider inngår ofte i prisen som er beregnet for en vare.</span><span class="sxs-lookup"><span data-stu-id="89ceb-181">Setup times are often part of the price that is calculated for an item.</span></span>  
5. <span data-ttu-id="89ceb-182">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="89ceb-182">Click Save.</span></span>
6. <span data-ttu-id="89ceb-183">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="89ceb-183">Close the page.</span></span>

