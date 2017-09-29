--- 
title: Opprette et produktnummer for konfigurerte produktvarianter
description: "Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard."
author: BibiSp
manager: AnnBe
ms.date: 10/25/2016
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
ms.openlocfilehash: e70a5f28635e75a69811085637f7e7431c0f1d40
ms.contentlocale: nb-no
ms.lasthandoff: 08/29/2017

---
# <a name="create-a-product-number-for-configured-product-variants"></a><span data-ttu-id="8bf18-103">Opprette et produktnummer for konfigurerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="8bf18-103">Create a product number for configured product variants</span></span>

[!include[task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="8bf18-104">Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard.</span><span class="sxs-lookup"><span data-stu-id="8bf18-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="8bf18-105">Prosedyren viser også hvordan du kan bygge konfigurasjonsterminologi for en komponent i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="8bf18-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="8bf18-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="8bf18-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="8bf18-107">Den nye produktnummerterminologien tilordnes til produktstandarden D0004.</span><span class="sxs-lookup"><span data-stu-id="8bf18-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="8bf18-108">Denne oppgaven vil vanligvis bli utført av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="8bf18-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="8bf18-109">Opprette produktnummerterminologi</span><span class="sxs-lookup"><span data-stu-id="8bf18-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="8bf18-110">Klikk Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="8bf18-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="8bf18-111">Klikk Produktterminologi.</span><span class="sxs-lookup"><span data-stu-id="8bf18-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="8bf18-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="8bf18-112">Click New.</span></span>
4. <span data-ttu-id="8bf18-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bf18-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="8bf18-114">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="8bf18-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="8bf18-115">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8bf18-115">Click Add.</span></span>
7. <span data-ttu-id="8bf18-116">Klikk Produktstandardnummer.</span><span class="sxs-lookup"><span data-stu-id="8bf18-116">Click Product master number.</span></span>
8. <span data-ttu-id="8bf18-117">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8bf18-117">Click Add.</span></span>
9. <span data-ttu-id="8bf18-118">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="8bf18-118">Click Text constant.</span></span>
10. <span data-ttu-id="8bf18-119">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8bf18-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="8bf18-120">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bf18-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="8bf18-121">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8bf18-121">Click Add.</span></span>
13. <span data-ttu-id="8bf18-122">Klikk Konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="8bf18-122">Click Configuration.</span></span>
14. <span data-ttu-id="8bf18-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8bf18-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="8bf18-124">Tilordne produktnummerterminologien til en produktstandard</span><span class="sxs-lookup"><span data-stu-id="8bf18-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="8bf18-125">Klikk Produktstandarder.</span><span class="sxs-lookup"><span data-stu-id="8bf18-125">Click Product masters.</span></span>
2. <span data-ttu-id="8bf18-126">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="8bf18-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="8bf18-127">Du kan for eksempel filtrere på Produktnummer-feltet med verdien D.</span><span class="sxs-lookup"><span data-stu-id="8bf18-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="8bf18-128">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8bf18-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8bf18-129">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="8bf18-129">Click Edit.</span></span>
5. <span data-ttu-id="8bf18-130">Velg Ja i feltet Bruk nomenklatur.</span><span class="sxs-lookup"><span data-stu-id="8bf18-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="8bf18-131">Angi eller velg en verdi i feltet Produktvariantnummerterminologi.</span><span class="sxs-lookup"><span data-stu-id="8bf18-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="8bf18-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8bf18-132">Close the page.</span></span>
8. <span data-ttu-id="8bf18-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8bf18-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="8bf18-134">Opprette terminologi for en komponent i en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="8bf18-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="8bf18-135">Klikk Produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="8bf18-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="8bf18-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="8bf18-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="8bf18-137">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8bf18-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="8bf18-138">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="8bf18-138">Click Edit.</span></span>
5. <span data-ttu-id="8bf18-139">Velg Ja i feltet Bruk konfigurasjonsnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="8bf18-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="8bf18-140">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8bf18-140">Click Add.</span></span>
7. <span data-ttu-id="8bf18-141">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="8bf18-141">Click Attribute value.</span></span>
8. <span data-ttu-id="8bf18-142">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8bf18-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="8bf18-143">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="8bf18-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="8bf18-144">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8bf18-144">Click Add.</span></span>
11. <span data-ttu-id="8bf18-145">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="8bf18-145">Click Text constant.</span></span>
12. <span data-ttu-id="8bf18-146">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8bf18-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="8bf18-147">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bf18-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="8bf18-148">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8bf18-148">Click Add.</span></span>
15. <span data-ttu-id="8bf18-149">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="8bf18-149">Click Attribute value.</span></span>
16. <span data-ttu-id="8bf18-150">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8bf18-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="8bf18-151">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="8bf18-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="8bf18-152">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8bf18-152">Click Add.</span></span>
19. <span data-ttu-id="8bf18-153">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="8bf18-153">Click Text constant.</span></span>
20. <span data-ttu-id="8bf18-154">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8bf18-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="8bf18-155">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bf18-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="8bf18-156">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8bf18-156">Click Add.</span></span>
23. <span data-ttu-id="8bf18-157">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="8bf18-157">Click Attribute value.</span></span>
24. <span data-ttu-id="8bf18-158">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8bf18-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="8bf18-159">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="8bf18-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="8bf18-160">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8bf18-160">Click Add.</span></span>
27. <span data-ttu-id="8bf18-161">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="8bf18-161">Click Text constant.</span></span>
28. <span data-ttu-id="8bf18-162">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8bf18-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="8bf18-163">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bf18-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="8bf18-164">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8bf18-164">Click Add.</span></span>
31. <span data-ttu-id="8bf18-165">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="8bf18-165">Click Attribute value.</span></span>
32. <span data-ttu-id="8bf18-166">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8bf18-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="8bf18-167">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="8bf18-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="8bf18-168">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8bf18-168">Click Add.</span></span>
35. <span data-ttu-id="8bf18-169">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="8bf18-169">Click Text constant.</span></span>
36. <span data-ttu-id="8bf18-170">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8bf18-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="8bf18-171">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bf18-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="8bf18-172">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="8bf18-172">Click Add.</span></span>
39. <span data-ttu-id="8bf18-173">Klikk Nummerserieverdi.</span><span class="sxs-lookup"><span data-stu-id="8bf18-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="8bf18-174">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="8bf18-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="8bf18-175">Angi eller velg en verdi i Nummerserieverdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="8bf18-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="8bf18-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8bf18-176">Close the page.</span></span>
43. <span data-ttu-id="8bf18-177">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8bf18-177">Close the page.</span></span>
44. <span data-ttu-id="8bf18-178">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="8bf18-178">Close the page.</span></span>


