--- 
title: Opprette en produktnummerterminologi for konfigurerte produktvarianter
description: "Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard."
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: 
ms.service: dynamics-ax-applications
ms.technology: 
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: shylaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.translationtype: HT
ms.sourcegitcommit: 0312b8cfadd45f8e59225e9daba78b9e216cff51
ms.openlocfilehash: 800afdf075f0675185514158f3b712a0fe7675e3
ms.contentlocale: nb-no
ms.lasthandoff: 10/16/2018

---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="82883-103">Opprette en produktnummerterminologi for konfigurerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="82883-103">Create a product number nomenclature for configured product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="82883-104">Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard.</span><span class="sxs-lookup"><span data-stu-id="82883-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="82883-105">Prosedyren viser også hvordan du kan bygge konfigurasjonsterminologi for en komponent i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="82883-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="82883-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="82883-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="82883-107">Den nye produktnummerterminologien tilordnes til produktstandarden D0004.</span><span class="sxs-lookup"><span data-stu-id="82883-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="82883-108">Denne oppgaven vil vanligvis bli utført av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="82883-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="82883-109">Opprette produktnummerterminologi</span><span class="sxs-lookup"><span data-stu-id="82883-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="82883-110">Klikk Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="82883-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="82883-111">Klikk Produktterminologi.</span><span class="sxs-lookup"><span data-stu-id="82883-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="82883-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="82883-112">Click New.</span></span>
4. <span data-ttu-id="82883-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="82883-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="82883-114">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="82883-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="82883-115">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="82883-115">Click Add.</span></span>
7. <span data-ttu-id="82883-116">Klikk Produktstandardnummer.</span><span class="sxs-lookup"><span data-stu-id="82883-116">Click Product master number.</span></span>
8. <span data-ttu-id="82883-117">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="82883-117">Click Add.</span></span>
9. <span data-ttu-id="82883-118">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="82883-118">Click Text constant.</span></span>
10. <span data-ttu-id="82883-119">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82883-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="82883-120">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="82883-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="82883-121">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="82883-121">Click Add.</span></span>
13. <span data-ttu-id="82883-122">Klikk Konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="82883-122">Click Configuration.</span></span>
14. <span data-ttu-id="82883-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82883-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="82883-124">Tilordne produktnummerterminologien til en produktstandard</span><span class="sxs-lookup"><span data-stu-id="82883-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="82883-125">Klikk Produktstandarder.</span><span class="sxs-lookup"><span data-stu-id="82883-125">Click Product masters.</span></span>
2. <span data-ttu-id="82883-126">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="82883-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="82883-127">Du kan for eksempel filtrere på Produktnummer-feltet med verdien D.</span><span class="sxs-lookup"><span data-stu-id="82883-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="82883-128">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82883-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="82883-129">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="82883-129">Click Edit.</span></span>
5. <span data-ttu-id="82883-130">Velg Ja i feltet Bruk nomenklatur.</span><span class="sxs-lookup"><span data-stu-id="82883-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="82883-131">Angi eller velg en verdi i feltet Produktvariantnummerterminologi.</span><span class="sxs-lookup"><span data-stu-id="82883-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="82883-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82883-132">Close the page.</span></span>
8. <span data-ttu-id="82883-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82883-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="82883-134">Opprette terminologi for en komponent i en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="82883-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="82883-135">Klikk Produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="82883-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="82883-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="82883-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="82883-137">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82883-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="82883-138">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="82883-138">Click Edit.</span></span>
5. <span data-ttu-id="82883-139">Velg Ja i feltet Bruk konfigurasjonsnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="82883-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="82883-140">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="82883-140">Click Add.</span></span>
7. <span data-ttu-id="82883-141">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="82883-141">Click Attribute value.</span></span>
8. <span data-ttu-id="82883-142">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82883-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="82883-143">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="82883-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="82883-144">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="82883-144">Click Add.</span></span>
11. <span data-ttu-id="82883-145">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="82883-145">Click Text constant.</span></span>
12. <span data-ttu-id="82883-146">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82883-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="82883-147">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="82883-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="82883-148">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="82883-148">Click Add.</span></span>
15. <span data-ttu-id="82883-149">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="82883-149">Click Attribute value.</span></span>
16. <span data-ttu-id="82883-150">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82883-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="82883-151">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="82883-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="82883-152">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="82883-152">Click Add.</span></span>
19. <span data-ttu-id="82883-153">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="82883-153">Click Text constant.</span></span>
20. <span data-ttu-id="82883-154">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82883-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="82883-155">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="82883-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="82883-156">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="82883-156">Click Add.</span></span>
23. <span data-ttu-id="82883-157">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="82883-157">Click Attribute value.</span></span>
24. <span data-ttu-id="82883-158">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82883-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="82883-159">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="82883-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="82883-160">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="82883-160">Click Add.</span></span>
27. <span data-ttu-id="82883-161">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="82883-161">Click Text constant.</span></span>
28. <span data-ttu-id="82883-162">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82883-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="82883-163">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="82883-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="82883-164">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="82883-164">Click Add.</span></span>
31. <span data-ttu-id="82883-165">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="82883-165">Click Attribute value.</span></span>
32. <span data-ttu-id="82883-166">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82883-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="82883-167">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="82883-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="82883-168">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="82883-168">Click Add.</span></span>
35. <span data-ttu-id="82883-169">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="82883-169">Click Text constant.</span></span>
36. <span data-ttu-id="82883-170">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82883-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="82883-171">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="82883-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="82883-172">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="82883-172">Click Add.</span></span>
39. <span data-ttu-id="82883-173">Klikk Nummerserieverdi.</span><span class="sxs-lookup"><span data-stu-id="82883-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="82883-174">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="82883-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="82883-175">Angi eller velg en verdi i Nummerserieverdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="82883-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="82883-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82883-176">Close the page.</span></span>
43. <span data-ttu-id="82883-177">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82883-177">Close the page.</span></span>
44. <span data-ttu-id="82883-178">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="82883-178">Close the page.</span></span>


