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
ms.sourcegitcommit: efcb77ff883b29a4bbaba27551e02311742afbbd
ms.openlocfilehash: 0fb1ed7b71912a867cd24634b4684de42f6f5efd
ms.contentlocale: nb-no
ms.lasthandoff: 05/08/2018

---
# <a name="create-a-product-number-for-configured-product-variants"></a><span data-ttu-id="32e34-103">Opprette et produktnummer for konfigurerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="32e34-103">Create a product number for configured product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="32e34-104">Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard.</span><span class="sxs-lookup"><span data-stu-id="32e34-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="32e34-105">Prosedyren viser også hvordan du kan bygge konfigurasjonsterminologi for en komponent i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="32e34-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="32e34-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="32e34-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="32e34-107">Den nye produktnummerterminologien tilordnes til produktstandarden D0004.</span><span class="sxs-lookup"><span data-stu-id="32e34-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="32e34-108">Denne oppgaven vil vanligvis bli utført av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="32e34-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="32e34-109">Opprette produktnummerterminologi</span><span class="sxs-lookup"><span data-stu-id="32e34-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="32e34-110">Klikk Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="32e34-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="32e34-111">Klikk Produktterminologi.</span><span class="sxs-lookup"><span data-stu-id="32e34-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="32e34-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="32e34-112">Click New.</span></span>
4. <span data-ttu-id="32e34-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="32e34-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="32e34-114">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="32e34-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="32e34-115">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="32e34-115">Click Add.</span></span>
7. <span data-ttu-id="32e34-116">Klikk Produktstandardnummer.</span><span class="sxs-lookup"><span data-stu-id="32e34-116">Click Product master number.</span></span>
8. <span data-ttu-id="32e34-117">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="32e34-117">Click Add.</span></span>
9. <span data-ttu-id="32e34-118">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="32e34-118">Click Text constant.</span></span>
10. <span data-ttu-id="32e34-119">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32e34-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="32e34-120">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="32e34-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="32e34-121">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="32e34-121">Click Add.</span></span>
13. <span data-ttu-id="32e34-122">Klikk Konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="32e34-122">Click Configuration.</span></span>
14. <span data-ttu-id="32e34-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="32e34-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="32e34-124">Tilordne produktnummerterminologien til en produktstandard</span><span class="sxs-lookup"><span data-stu-id="32e34-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="32e34-125">Klikk Produktstandarder.</span><span class="sxs-lookup"><span data-stu-id="32e34-125">Click Product masters.</span></span>
2. <span data-ttu-id="32e34-126">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="32e34-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="32e34-127">Du kan for eksempel filtrere på Produktnummer-feltet med verdien D.</span><span class="sxs-lookup"><span data-stu-id="32e34-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="32e34-128">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32e34-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="32e34-129">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="32e34-129">Click Edit.</span></span>
5. <span data-ttu-id="32e34-130">Velg Ja i feltet Bruk nomenklatur.</span><span class="sxs-lookup"><span data-stu-id="32e34-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="32e34-131">Angi eller velg en verdi i feltet Produktvariantnummerterminologi.</span><span class="sxs-lookup"><span data-stu-id="32e34-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="32e34-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="32e34-132">Close the page.</span></span>
8. <span data-ttu-id="32e34-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="32e34-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="32e34-134">Opprette terminologi for en komponent i en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="32e34-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="32e34-135">Klikk Produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="32e34-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="32e34-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="32e34-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="32e34-137">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32e34-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="32e34-138">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="32e34-138">Click Edit.</span></span>
5. <span data-ttu-id="32e34-139">Velg Ja i feltet Bruk konfigurasjonsnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="32e34-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="32e34-140">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="32e34-140">Click Add.</span></span>
7. <span data-ttu-id="32e34-141">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="32e34-141">Click Attribute value.</span></span>
8. <span data-ttu-id="32e34-142">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32e34-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="32e34-143">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="32e34-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="32e34-144">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="32e34-144">Click Add.</span></span>
11. <span data-ttu-id="32e34-145">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="32e34-145">Click Text constant.</span></span>
12. <span data-ttu-id="32e34-146">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32e34-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="32e34-147">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="32e34-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="32e34-148">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="32e34-148">Click Add.</span></span>
15. <span data-ttu-id="32e34-149">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="32e34-149">Click Attribute value.</span></span>
16. <span data-ttu-id="32e34-150">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32e34-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="32e34-151">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="32e34-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="32e34-152">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="32e34-152">Click Add.</span></span>
19. <span data-ttu-id="32e34-153">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="32e34-153">Click Text constant.</span></span>
20. <span data-ttu-id="32e34-154">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32e34-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="32e34-155">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="32e34-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="32e34-156">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="32e34-156">Click Add.</span></span>
23. <span data-ttu-id="32e34-157">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="32e34-157">Click Attribute value.</span></span>
24. <span data-ttu-id="32e34-158">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32e34-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="32e34-159">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="32e34-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="32e34-160">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="32e34-160">Click Add.</span></span>
27. <span data-ttu-id="32e34-161">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="32e34-161">Click Text constant.</span></span>
28. <span data-ttu-id="32e34-162">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32e34-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="32e34-163">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="32e34-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="32e34-164">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="32e34-164">Click Add.</span></span>
31. <span data-ttu-id="32e34-165">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="32e34-165">Click Attribute value.</span></span>
32. <span data-ttu-id="32e34-166">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32e34-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="32e34-167">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="32e34-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="32e34-168">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="32e34-168">Click Add.</span></span>
35. <span data-ttu-id="32e34-169">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="32e34-169">Click Text constant.</span></span>
36. <span data-ttu-id="32e34-170">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32e34-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="32e34-171">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="32e34-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="32e34-172">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="32e34-172">Click Add.</span></span>
39. <span data-ttu-id="32e34-173">Klikk Nummerserieverdi.</span><span class="sxs-lookup"><span data-stu-id="32e34-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="32e34-174">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="32e34-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="32e34-175">Angi eller velg en verdi i Nummerserieverdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="32e34-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="32e34-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="32e34-176">Close the page.</span></span>
43. <span data-ttu-id="32e34-177">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="32e34-177">Close the page.</span></span>
44. <span data-ttu-id="32e34-178">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="32e34-178">Close the page.</span></span>


