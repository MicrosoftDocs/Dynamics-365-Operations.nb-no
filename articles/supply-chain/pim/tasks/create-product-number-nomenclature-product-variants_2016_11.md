---
title: Opprette en produktnummerterminologi for konfigurerte produktvarianter
description: Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 07922a20d5c99640f32bb28ddddaffe846440667
ms.sourcegitcommit: eaf330dbee1db96c20d5ac479f007747bea079eb
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 02/15/2021
ms.locfileid: "5258881"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="3ea46-103">Opprette en produktnummerterminologi for konfigurerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="3ea46-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3ea46-104">Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard.</span><span class="sxs-lookup"><span data-stu-id="3ea46-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="3ea46-105">Prosedyren viser også hvordan du kan bygge konfigurasjonsterminologi for en komponent i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="3ea46-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="3ea46-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="3ea46-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3ea46-107">Den nye produktnummerterminologien tilordnes til produktstandarden D0004.</span><span class="sxs-lookup"><span data-stu-id="3ea46-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="3ea46-108">Denne oppgaven vil vanligvis bli utført av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="3ea46-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="3ea46-109">Opprette produktnummerterminologi</span><span class="sxs-lookup"><span data-stu-id="3ea46-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="3ea46-110">Klikk på Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="3ea46-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="3ea46-111">Klikk på Produktterminologi.</span><span class="sxs-lookup"><span data-stu-id="3ea46-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="3ea46-112">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="3ea46-112">Click New.</span></span>
4. <span data-ttu-id="3ea46-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="3ea46-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3ea46-114">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3ea46-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="3ea46-115">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3ea46-115">Click Add.</span></span>
7. <span data-ttu-id="3ea46-116">Klikk på Produktstandardnummer.</span><span class="sxs-lookup"><span data-stu-id="3ea46-116">Click Product master number.</span></span>
8. <span data-ttu-id="3ea46-117">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3ea46-117">Click Add.</span></span>
9. <span data-ttu-id="3ea46-118">Klikk på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="3ea46-118">Click Text constant.</span></span>
10. <span data-ttu-id="3ea46-119">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3ea46-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="3ea46-120">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="3ea46-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="3ea46-121">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3ea46-121">Click Add.</span></span>
13. <span data-ttu-id="3ea46-122">Klikk på Konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="3ea46-122">Click Configuration.</span></span>
14. <span data-ttu-id="3ea46-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3ea46-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="3ea46-124">Tilordne produktnummerterminologien til en produktstandard</span><span class="sxs-lookup"><span data-stu-id="3ea46-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="3ea46-125">Klikk på Produktstandarder.</span><span class="sxs-lookup"><span data-stu-id="3ea46-125">Click Product masters.</span></span>
2. <span data-ttu-id="3ea46-126">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="3ea46-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3ea46-127">Du kan for eksempel filtrere på Produktnummer-feltet med verdien D.</span><span class="sxs-lookup"><span data-stu-id="3ea46-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="3ea46-128">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3ea46-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3ea46-129">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="3ea46-129">Click Edit.</span></span>
5. <span data-ttu-id="3ea46-130">Velg Ja i feltet Bruk nomenklatur.</span><span class="sxs-lookup"><span data-stu-id="3ea46-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="3ea46-131">Angi eller velg en verdi i feltet Produktvariantnummerterminologi.</span><span class="sxs-lookup"><span data-stu-id="3ea46-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="3ea46-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3ea46-132">Close the page.</span></span>
8. <span data-ttu-id="3ea46-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3ea46-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="3ea46-134">Opprette terminologi for en komponent i en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="3ea46-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="3ea46-135">Klikk på Produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="3ea46-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="3ea46-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3ea46-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3ea46-137">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3ea46-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3ea46-138">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="3ea46-138">Click Edit.</span></span>
5. <span data-ttu-id="3ea46-139">Velg Ja i feltet Bruk konfigurasjonsnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="3ea46-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="3ea46-140">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3ea46-140">Click Add.</span></span>
7. <span data-ttu-id="3ea46-141">Klikk på Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="3ea46-141">Click Attribute value.</span></span>
8. <span data-ttu-id="3ea46-142">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3ea46-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3ea46-143">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="3ea46-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="3ea46-144">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3ea46-144">Click Add.</span></span>
11. <span data-ttu-id="3ea46-145">Klikk på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="3ea46-145">Click Text constant.</span></span>
12. <span data-ttu-id="3ea46-146">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3ea46-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="3ea46-147">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="3ea46-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="3ea46-148">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3ea46-148">Click Add.</span></span>
15. <span data-ttu-id="3ea46-149">Klikk på Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="3ea46-149">Click Attribute value.</span></span>
16. <span data-ttu-id="3ea46-150">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3ea46-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="3ea46-151">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="3ea46-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="3ea46-152">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3ea46-152">Click Add.</span></span>
19. <span data-ttu-id="3ea46-153">Klikk på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="3ea46-153">Click Text constant.</span></span>
20. <span data-ttu-id="3ea46-154">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3ea46-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="3ea46-155">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="3ea46-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="3ea46-156">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3ea46-156">Click Add.</span></span>
23. <span data-ttu-id="3ea46-157">Klikk på Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="3ea46-157">Click Attribute value.</span></span>
24. <span data-ttu-id="3ea46-158">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3ea46-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="3ea46-159">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="3ea46-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="3ea46-160">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3ea46-160">Click Add.</span></span>
27. <span data-ttu-id="3ea46-161">Klikk på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="3ea46-161">Click Text constant.</span></span>
28. <span data-ttu-id="3ea46-162">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3ea46-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="3ea46-163">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="3ea46-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="3ea46-164">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3ea46-164">Click Add.</span></span>
31. <span data-ttu-id="3ea46-165">Klikk på Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="3ea46-165">Click Attribute value.</span></span>
32. <span data-ttu-id="3ea46-166">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3ea46-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="3ea46-167">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="3ea46-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="3ea46-168">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3ea46-168">Click Add.</span></span>
35. <span data-ttu-id="3ea46-169">Klikk på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="3ea46-169">Click Text constant.</span></span>
36. <span data-ttu-id="3ea46-170">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3ea46-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="3ea46-171">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="3ea46-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="3ea46-172">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3ea46-172">Click Add.</span></span>
39. <span data-ttu-id="3ea46-173">Klikk på Nummerserieverdi.</span><span class="sxs-lookup"><span data-stu-id="3ea46-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="3ea46-174">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3ea46-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="3ea46-175">Angi eller velg en verdi i Nummerserieverdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="3ea46-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="3ea46-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3ea46-176">Close the page.</span></span>
43. <span data-ttu-id="3ea46-177">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3ea46-177">Close the page.</span></span>
44. <span data-ttu-id="3ea46-178">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3ea46-178">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]