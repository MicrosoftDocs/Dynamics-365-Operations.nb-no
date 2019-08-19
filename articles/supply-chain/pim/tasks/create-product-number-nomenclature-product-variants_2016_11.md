---
title: Opprette en produktnummerterminologi for konfigurerte produktvarianter
description: Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 22aa4823fbf43b29a8fd9661645e8563c07e437d
ms.sourcegitcommit: 8b4b6a9226d4e5f66498ab2a5b4160e26dd112af
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 08/01/2019
ms.locfileid: "1844663"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="0c38f-103">Opprette en produktnummerterminologi for konfigurerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="0c38f-103">Create a product number nomenclature for configured product variants</span></span>

[!include [task guide banner](../../includes/task-guide-banner.md)]

<span data-ttu-id="0c38f-104">Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard.</span><span class="sxs-lookup"><span data-stu-id="0c38f-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="0c38f-105">Prosedyren viser også hvordan du kan bygge konfigurasjonsterminologi for en komponent i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="0c38f-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="0c38f-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="0c38f-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="0c38f-107">Den nye produktnummerterminologien tilordnes til produktstandarden D0004.</span><span class="sxs-lookup"><span data-stu-id="0c38f-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="0c38f-108">Denne oppgaven vil vanligvis bli utført av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="0c38f-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="0c38f-109">Opprette produktnummerterminologi</span><span class="sxs-lookup"><span data-stu-id="0c38f-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="0c38f-110">Klikk Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="0c38f-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="0c38f-111">Klikk Produktterminologi.</span><span class="sxs-lookup"><span data-stu-id="0c38f-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="0c38f-112">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="0c38f-112">Click New.</span></span>
4. <span data-ttu-id="0c38f-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="0c38f-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="0c38f-114">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="0c38f-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="0c38f-115">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0c38f-115">Click Add.</span></span>
7. <span data-ttu-id="0c38f-116">Klikk Produktstandardnummer.</span><span class="sxs-lookup"><span data-stu-id="0c38f-116">Click Product master number.</span></span>
8. <span data-ttu-id="0c38f-117">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0c38f-117">Click Add.</span></span>
9. <span data-ttu-id="0c38f-118">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="0c38f-118">Click Text constant.</span></span>
10. <span data-ttu-id="0c38f-119">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0c38f-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="0c38f-120">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="0c38f-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="0c38f-121">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0c38f-121">Click Add.</span></span>
13. <span data-ttu-id="0c38f-122">Klikk Konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="0c38f-122">Click Configuration.</span></span>
14. <span data-ttu-id="0c38f-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0c38f-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="0c38f-124">Tilordne produktnummerterminologien til en produktstandard</span><span class="sxs-lookup"><span data-stu-id="0c38f-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="0c38f-125">Klikk Produktstandarder.</span><span class="sxs-lookup"><span data-stu-id="0c38f-125">Click Product masters.</span></span>
2. <span data-ttu-id="0c38f-126">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="0c38f-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="0c38f-127">Du kan for eksempel filtrere på Produktnummer-feltet med verdien D.</span><span class="sxs-lookup"><span data-stu-id="0c38f-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="0c38f-128">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0c38f-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0c38f-129">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="0c38f-129">Click Edit.</span></span>
5. <span data-ttu-id="0c38f-130">Velg Ja i feltet Bruk nomenklatur.</span><span class="sxs-lookup"><span data-stu-id="0c38f-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="0c38f-131">Angi eller velg en verdi i feltet Produktvariantnummerterminologi.</span><span class="sxs-lookup"><span data-stu-id="0c38f-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="0c38f-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0c38f-132">Close the page.</span></span>
8. <span data-ttu-id="0c38f-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0c38f-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="0c38f-134">Opprette terminologi for en komponent i en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="0c38f-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="0c38f-135">Klikk Produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="0c38f-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="0c38f-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="0c38f-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="0c38f-137">Klikk koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0c38f-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="0c38f-138">Klikk Rediger.</span><span class="sxs-lookup"><span data-stu-id="0c38f-138">Click Edit.</span></span>
5. <span data-ttu-id="0c38f-139">Velg Ja i feltet Bruk konfigurasjonsnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="0c38f-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="0c38f-140">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0c38f-140">Click Add.</span></span>
7. <span data-ttu-id="0c38f-141">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="0c38f-141">Click Attribute value.</span></span>
8. <span data-ttu-id="0c38f-142">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0c38f-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="0c38f-143">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="0c38f-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="0c38f-144">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0c38f-144">Click Add.</span></span>
11. <span data-ttu-id="0c38f-145">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="0c38f-145">Click Text constant.</span></span>
12. <span data-ttu-id="0c38f-146">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0c38f-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="0c38f-147">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="0c38f-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="0c38f-148">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0c38f-148">Click Add.</span></span>
15. <span data-ttu-id="0c38f-149">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="0c38f-149">Click Attribute value.</span></span>
16. <span data-ttu-id="0c38f-150">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0c38f-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="0c38f-151">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="0c38f-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="0c38f-152">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0c38f-152">Click Add.</span></span>
19. <span data-ttu-id="0c38f-153">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="0c38f-153">Click Text constant.</span></span>
20. <span data-ttu-id="0c38f-154">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0c38f-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="0c38f-155">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="0c38f-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="0c38f-156">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0c38f-156">Click Add.</span></span>
23. <span data-ttu-id="0c38f-157">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="0c38f-157">Click Attribute value.</span></span>
24. <span data-ttu-id="0c38f-158">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0c38f-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="0c38f-159">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="0c38f-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="0c38f-160">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0c38f-160">Click Add.</span></span>
27. <span data-ttu-id="0c38f-161">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="0c38f-161">Click Text constant.</span></span>
28. <span data-ttu-id="0c38f-162">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0c38f-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="0c38f-163">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="0c38f-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="0c38f-164">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0c38f-164">Click Add.</span></span>
31. <span data-ttu-id="0c38f-165">Klikk Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="0c38f-165">Click Attribute value.</span></span>
32. <span data-ttu-id="0c38f-166">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0c38f-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="0c38f-167">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="0c38f-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="0c38f-168">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0c38f-168">Click Add.</span></span>
35. <span data-ttu-id="0c38f-169">Klikk Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="0c38f-169">Click Text constant.</span></span>
36. <span data-ttu-id="0c38f-170">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0c38f-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="0c38f-171">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="0c38f-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="0c38f-172">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="0c38f-172">Click Add.</span></span>
39. <span data-ttu-id="0c38f-173">Klikk Nummerserieverdi.</span><span class="sxs-lookup"><span data-stu-id="0c38f-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="0c38f-174">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="0c38f-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="0c38f-175">Angi eller velg en verdi i Nummerserieverdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="0c38f-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="0c38f-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0c38f-176">Close the page.</span></span>
43. <span data-ttu-id="0c38f-177">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0c38f-177">Close the page.</span></span>
44. <span data-ttu-id="0c38f-178">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="0c38f-178">Close the page.</span></span>

