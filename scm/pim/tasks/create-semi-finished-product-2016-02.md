--- 
title: Opprette et halvfabrikata (bare februar 2016)
description: "Denne oppgaven fokuserer på å opprette et halvfabrikata."
author: YuyuScheller
manager: AnnBe
ms.date: 02/07/2017
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
audience: Application User
ms.reviewer: yuyus
ms.search.scope: Operations
ms.search.region: Global
ms.author: yuyus
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: AX 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 663da58ef01b705c0c984fbfd3fce8bc31be04c6
ms.openlocfilehash: 038d8cd9333635d3269bb4f62a5402c2309bfd3c
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-semi-finished-product-february-2016-only"></a><span data-ttu-id="f1c79-103">Opprette et halvfabrikata (bare februar 2016)</span><span class="sxs-lookup"><span data-stu-id="f1c79-103">Create a semi-finished product (February 2016 only)</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="f1c79-104">Denne oppgaven fokuserer på å opprette et halvfabrikata.</span><span class="sxs-lookup"><span data-stu-id="f1c79-104">This task focuses on creating a semi-finished product.</span></span> <span data-ttu-id="f1c79-105">Det er den andre oppgaven i serien stykklisteberegning.</span><span class="sxs-lookup"><span data-stu-id="f1c79-105">It is the second task in the BOM calculation series.</span></span> <span data-ttu-id="f1c79-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne oppgaven.</span><span class="sxs-lookup"><span data-stu-id="f1c79-106">The demo data company used to create this task is USMF.</span></span>

1. <span data-ttu-id="f1c79-107">Gå til Behandling av produktinformasjon > Produkter > Frigitte produkter.</span><span class="sxs-lookup"><span data-stu-id="f1c79-107">Go to Product information management > Products > Released products.</span></span>
2. <span data-ttu-id="f1c79-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f1c79-108">Click New.</span></span>
3. <span data-ttu-id="f1c79-109">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="f1c79-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="f1c79-110">I dette eksemplet skriver du inn BOM_2.</span><span class="sxs-lookup"><span data-stu-id="f1c79-110">For this example, type BOM_2.</span></span>  
4. <span data-ttu-id="f1c79-111">Angi eller velg en verdi i Varemodellgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-111">In the Item model group field, enter or select a value.</span></span>
    * <span data-ttu-id="f1c79-112">Velg STD.</span><span class="sxs-lookup"><span data-stu-id="f1c79-112">Select STD.</span></span> <span data-ttu-id="f1c79-113">STD står for standardkostnad, og er den mest brukte modellen når du arbeider med kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="f1c79-113">STD stands for standard cost and is the most commonly used model when working with cost calculations.</span></span>  
5. <span data-ttu-id="f1c79-114">Angi eller velg en verdi i Varegruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-114">In the Item group field, enter or select a value.</span></span>
    * <span data-ttu-id="f1c79-115">Velg for eksempel Lyd.</span><span class="sxs-lookup"><span data-stu-id="f1c79-115">For example, select Audio.</span></span> <span data-ttu-id="f1c79-116">Dette har ingen innvirkning på kostnadsberegninger.</span><span class="sxs-lookup"><span data-stu-id="f1c79-116">This has no impact on cost calculations.</span></span>  
6. <span data-ttu-id="f1c79-117">Angi eller velg en verdi i lagringsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-117">In the Storage dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f1c79-118">Velg SiteWH.</span><span class="sxs-lookup"><span data-stu-id="f1c79-118">Select SiteWH.</span></span> <span data-ttu-id="f1c79-119">Bare Område og Lager blir brukt i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-119">Only Site and Warehouse will be used for this example.</span></span>  
7. <span data-ttu-id="f1c79-120">Angi eller velg en verdi i sporingsdimensjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-120">In the Tracking dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="f1c79-121">Sporingsdimensjoner vil ikke bli brukt i dette eksemplet, så velg Ingen.</span><span class="sxs-lookup"><span data-stu-id="f1c79-121">Tracking dimensions will not be used for this example, select None.</span></span>  
8. <span data-ttu-id="f1c79-122">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="f1c79-122">Click OK.</span></span>
9. <span data-ttu-id="f1c79-123">Klikk Administrer lager i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f1c79-123">On the Action Pane, click Manage inventory.</span></span>
10. <span data-ttu-id="f1c79-124">Klikk Standard ordreinnstillinger.</span><span class="sxs-lookup"><span data-stu-id="f1c79-124">Click Default order settings.</span></span>
11. <span data-ttu-id="f1c79-125">Velg Produksjon i feltet Standard ordretype.</span><span class="sxs-lookup"><span data-stu-id="f1c79-125">In the Default order type field, select 'Production'.</span></span>
    * <span data-ttu-id="f1c79-126">Siden dette er et halvfabrikata som skal produseres, velger du Produksjon.</span><span class="sxs-lookup"><span data-stu-id="f1c79-126">Because this is a semi-finished product that will be produced, select Production.</span></span>  
12. <span data-ttu-id="f1c79-127">Angi eller velg en verdi i feltet Innkjøpssite.</span><span class="sxs-lookup"><span data-stu-id="f1c79-127">In the Purchase site field, enter or select a value.</span></span>
    * <span data-ttu-id="f1c79-128">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-128">For this example, select Site 1.</span></span>  
13. <span data-ttu-id="f1c79-129">Angi eller velg en verdi i feltet Lagersite.</span><span class="sxs-lookup"><span data-stu-id="f1c79-129">In the Inventory site field, enter or select a value.</span></span>
    * <span data-ttu-id="f1c79-130">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-130">For this example, select Site 1.</span></span>  
14. <span data-ttu-id="f1c79-131">Angi eller velg en verdi i feltet Salgssite.</span><span class="sxs-lookup"><span data-stu-id="f1c79-131">In the Sales site field, enter or select a value.</span></span>
    * <span data-ttu-id="f1c79-132">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-132">For this example, select Site 1.</span></span>  
15. <span data-ttu-id="f1c79-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f1c79-133">Close the page.</span></span>
16. <span data-ttu-id="f1c79-134">Klikk Styr kostnader i handlingsruten.</span><span class="sxs-lookup"><span data-stu-id="f1c79-134">On the Action Pane, click Manage costs.</span></span>
17. <span data-ttu-id="f1c79-135">Klikk Varepris.</span><span class="sxs-lookup"><span data-stu-id="f1c79-135">Click Item price.</span></span>
18. <span data-ttu-id="f1c79-136">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="f1c79-136">Click New.</span></span>
19. <span data-ttu-id="f1c79-137">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f1c79-137">In the list, mark the selected row.</span></span>
20. <span data-ttu-id="f1c79-138">Angi eller velg en verdi i Versjon-feltet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-138">In the Version field, enter or select a value.</span></span>
    * <span data-ttu-id="f1c79-139">Velg Versjon 10 i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-139">For this example, select Version 10.</span></span>  
21. <span data-ttu-id="f1c79-140">Angi eller velg en verdi i Område-feltet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-140">In the Site field, enter or select a value.</span></span>
    * <span data-ttu-id="f1c79-141">Velg Område 1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-141">For this example, select Site 1.</span></span>  
22. <span data-ttu-id="f1c79-142">Sett Pris til 10.</span><span class="sxs-lookup"><span data-stu-id="f1c79-142">Set Price to '10'.</span></span>
    * <span data-ttu-id="f1c79-143">Skriv inn en kostpris på 10 i dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-143">For this example, type a cost price of 10.</span></span>  
23. <span data-ttu-id="f1c79-144">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="f1c79-144">Click Save.</span></span>
24. <span data-ttu-id="f1c79-145">Klikk Aktiver ventende pris(er).</span><span class="sxs-lookup"><span data-stu-id="f1c79-145">Click Activate pending price(s).</span></span>
25. <span data-ttu-id="f1c79-146">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f1c79-146">Close the page.</span></span>
26. <span data-ttu-id="f1c79-147">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f1c79-147">Close the page.</span></span>
27. <span data-ttu-id="f1c79-148">Klikk BOM_2 for å åpne den.</span><span class="sxs-lookup"><span data-stu-id="f1c79-148">Click BOM_2 to open it.</span></span>
28. <span data-ttu-id="f1c79-149">Vis delen Styr kostnader.</span><span class="sxs-lookup"><span data-stu-id="f1c79-149">Expand the Manage costs section.</span></span>
29. <span data-ttu-id="f1c79-150">Angi eller velg en verdi i Kostgruppe-feltet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-150">In the Cost group field, enter or select a value.</span></span>
    * <span data-ttu-id="f1c79-151">Velg Kostgruppe M1 for dette eksemplet.</span><span class="sxs-lookup"><span data-stu-id="f1c79-151">For this example, select Cost group M1.</span></span>  
30. <span data-ttu-id="f1c79-152">Bruk snarveien for å lagre en post.</span><span class="sxs-lookup"><span data-stu-id="f1c79-152">Use the shortcut for saving a record.</span></span>
31. <span data-ttu-id="f1c79-153">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="f1c79-153">Close the page.</span></span>


