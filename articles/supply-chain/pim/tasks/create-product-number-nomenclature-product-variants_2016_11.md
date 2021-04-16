---
title: Opprette en produktnummerterminologi for konfigurerte produktvarianter
description: Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, EcoResNomenclature, EcoResProductListPage, EcoResProductDetails, PCProductConfigurationModelListPage, PCProductConfigurationModelDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: f342831d95f9988f9bb7807bac986e43cb317e0f
ms.sourcegitcommit: 0e8db169c3f90bd750826af76709ef5d621fd377
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/01/2021
ms.locfileid: "5820015"
---
# <a name="create-a-product-number-nomenclature-for-configured-product-variants"></a><span data-ttu-id="3fff6-103">Opprette en produktnummerterminologi for konfigurerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="3fff6-103">Create a product number nomenclature for configured product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="3fff6-104">Denne fremgangsmåten viser hvordan du setter opp produktnummerterminologi for konfigurerte produktvarianter, og hvordan denne kan knyttes til en konfigurerbar produktstandard.</span><span class="sxs-lookup"><span data-stu-id="3fff6-104">This procedure shows you how to set up a product number nomenclature for configured product variants, and how it can be attached to a configurable product master.</span></span> <span data-ttu-id="3fff6-105">Prosedyren viser også hvordan du kan bygge konfigurasjonsterminologi for en komponent i en produktkonfigurasjonsmodell.</span><span class="sxs-lookup"><span data-stu-id="3fff6-105">This procedure also demonstrates how you can build a configuration nomenclature for a product configuration model component.</span></span> <span data-ttu-id="3fff6-106">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="3fff6-106">The demo data company used to create this procedure is USMF.</span></span> <span data-ttu-id="3fff6-107">Den nye produktnummerterminologien tilordnes til produktstandarden D0004.</span><span class="sxs-lookup"><span data-stu-id="3fff6-107">The new product number nomenclature is assigned to the D0004 product master.</span></span> <span data-ttu-id="3fff6-108">Denne oppgaven vil vanligvis bli utført av en produktdesigner.</span><span class="sxs-lookup"><span data-stu-id="3fff6-108">This task would typically be done by a product designer.</span></span>


## <a name="create-a-product-number-nomenclature"></a><span data-ttu-id="3fff6-109">Opprette produktnummerterminologi</span><span class="sxs-lookup"><span data-stu-id="3fff6-109">Create a product number nomenclature</span></span>
1. <span data-ttu-id="3fff6-110">Klikk på Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="3fff6-110">Click Product variant model definition.</span></span>
2. <span data-ttu-id="3fff6-111">Klikk på Produktterminologi.</span><span class="sxs-lookup"><span data-stu-id="3fff6-111">Click Product nomenclature.</span></span>
3. <span data-ttu-id="3fff6-112">Klikk på Ny.</span><span class="sxs-lookup"><span data-stu-id="3fff6-112">Click New.</span></span>
4. <span data-ttu-id="3fff6-113">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="3fff6-113">In the Name field, type a value.</span></span>
5. <span data-ttu-id="3fff6-114">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="3fff6-114">In the Description field, type a value.</span></span>
6. <span data-ttu-id="3fff6-115">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3fff6-115">Click Add.</span></span>
7. <span data-ttu-id="3fff6-116">Klikk på Produktstandardnummer.</span><span class="sxs-lookup"><span data-stu-id="3fff6-116">Click Product master number.</span></span>
8. <span data-ttu-id="3fff6-117">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3fff6-117">Click Add.</span></span>
9. <span data-ttu-id="3fff6-118">Klikk på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="3fff6-118">Click Text constant.</span></span>
10. <span data-ttu-id="3fff6-119">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3fff6-119">In the list, mark the selected row.</span></span>
11. <span data-ttu-id="3fff6-120">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="3fff6-120">In the Text field, type a value.</span></span>
12. <span data-ttu-id="3fff6-121">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3fff6-121">Click Add.</span></span>
13. <span data-ttu-id="3fff6-122">Klikk på Konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="3fff6-122">Click Configuration.</span></span>
14. <span data-ttu-id="3fff6-123">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3fff6-123">Close the page.</span></span>

## <a name="assign-the-product-number-nomenclature-to-a-product-master"></a><span data-ttu-id="3fff6-124">Tilordne produktnummerterminologien til en produktstandard</span><span class="sxs-lookup"><span data-stu-id="3fff6-124">Assign the product number nomenclature to a product master</span></span>
1. <span data-ttu-id="3fff6-125">Klikk på Produktstandarder.</span><span class="sxs-lookup"><span data-stu-id="3fff6-125">Click Product masters.</span></span>
2. <span data-ttu-id="3fff6-126">Bruk hurtigfilteret for å søke etter poster.</span><span class="sxs-lookup"><span data-stu-id="3fff6-126">Use the Quick Filter to find records.</span></span> <span data-ttu-id="3fff6-127">Du kan for eksempel filtrere på Produktnummer-feltet med verdien D.</span><span class="sxs-lookup"><span data-stu-id="3fff6-127">For example, filter on the Product number field with a value of 'D'.</span></span>
3. <span data-ttu-id="3fff6-128">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3fff6-128">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3fff6-129">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="3fff6-129">Click Edit.</span></span>
5. <span data-ttu-id="3fff6-130">Velg Ja i feltet Bruk nomenklatur.</span><span class="sxs-lookup"><span data-stu-id="3fff6-130">Select Yes in the Use nomenclature field.</span></span>
6. <span data-ttu-id="3fff6-131">Angi eller velg en verdi i feltet Produktvariantnummerterminologi.</span><span class="sxs-lookup"><span data-stu-id="3fff6-131">In the Product variant number nomenclature field, enter or select a value.</span></span>
7. <span data-ttu-id="3fff6-132">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3fff6-132">Close the page.</span></span>
8. <span data-ttu-id="3fff6-133">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3fff6-133">Close the page.</span></span>

## <a name="create-nomenclature-for-a-product-configuration-model-component"></a><span data-ttu-id="3fff6-134">Opprette terminologi for en komponent i en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="3fff6-134">Create nomenclature for a product configuration model component</span></span>
1. <span data-ttu-id="3fff6-135">Klikk på Produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="3fff6-135">Click Product configuration models.</span></span>
2. <span data-ttu-id="3fff6-136">Finn og velg ønsket post i listen.</span><span class="sxs-lookup"><span data-stu-id="3fff6-136">In the list, find and select the desired record.</span></span>
3. <span data-ttu-id="3fff6-137">Klikk på koblingen i den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3fff6-137">In the list, click the link in the selected row.</span></span>
4. <span data-ttu-id="3fff6-138">Klikk på Rediger.</span><span class="sxs-lookup"><span data-stu-id="3fff6-138">Click Edit.</span></span>
5. <span data-ttu-id="3fff6-139">Velg Ja i feltet Bruk konfigurasjonsnomenklatur.</span><span class="sxs-lookup"><span data-stu-id="3fff6-139">Select Yes in the Use configuration nomenclature field.</span></span>
6. <span data-ttu-id="3fff6-140">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3fff6-140">Click Add.</span></span>
7. <span data-ttu-id="3fff6-141">Klikk på Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="3fff6-141">Click Attribute value.</span></span>
8. <span data-ttu-id="3fff6-142">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3fff6-142">In the list, mark the selected row.</span></span>
9. <span data-ttu-id="3fff6-143">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="3fff6-143">In the Attribute field, enter or select a value.</span></span>
10. <span data-ttu-id="3fff6-144">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3fff6-144">Click Add.</span></span>
11. <span data-ttu-id="3fff6-145">Klikk på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="3fff6-145">Click Text constant.</span></span>
12. <span data-ttu-id="3fff6-146">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3fff6-146">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="3fff6-147">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="3fff6-147">In the Text field, type a value.</span></span>
14. <span data-ttu-id="3fff6-148">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3fff6-148">Click Add.</span></span>
15. <span data-ttu-id="3fff6-149">Klikk på Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="3fff6-149">Click Attribute value.</span></span>
16. <span data-ttu-id="3fff6-150">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3fff6-150">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="3fff6-151">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="3fff6-151">In the Attribute field, enter or select a value.</span></span>
18. <span data-ttu-id="3fff6-152">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3fff6-152">Click Add.</span></span>
19. <span data-ttu-id="3fff6-153">Klikk på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="3fff6-153">Click Text constant.</span></span>
20. <span data-ttu-id="3fff6-154">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3fff6-154">In the list, mark the selected row.</span></span>
21. <span data-ttu-id="3fff6-155">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="3fff6-155">In the Text field, type a value.</span></span>
22. <span data-ttu-id="3fff6-156">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3fff6-156">Click Add.</span></span>
23. <span data-ttu-id="3fff6-157">Klikk på Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="3fff6-157">Click Attribute value.</span></span>
24. <span data-ttu-id="3fff6-158">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3fff6-158">In the list, mark the selected row.</span></span>
25. <span data-ttu-id="3fff6-159">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="3fff6-159">In the Attribute field, enter or select a value.</span></span>
26. <span data-ttu-id="3fff6-160">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3fff6-160">Click Add.</span></span>
27. <span data-ttu-id="3fff6-161">Klikk på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="3fff6-161">Click Text constant.</span></span>
28. <span data-ttu-id="3fff6-162">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3fff6-162">In the list, mark the selected row.</span></span>
29. <span data-ttu-id="3fff6-163">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="3fff6-163">In the Text field, type a value.</span></span>
30. <span data-ttu-id="3fff6-164">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3fff6-164">Click Add.</span></span>
31. <span data-ttu-id="3fff6-165">Klikk på Attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="3fff6-165">Click Attribute value.</span></span>
32. <span data-ttu-id="3fff6-166">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3fff6-166">In the list, mark the selected row.</span></span>
33. <span data-ttu-id="3fff6-167">Angi eller velg en verdi i feltet Attributt.</span><span class="sxs-lookup"><span data-stu-id="3fff6-167">In the Attribute field, enter or select a value.</span></span>
34. <span data-ttu-id="3fff6-168">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3fff6-168">Click Add.</span></span>
35. <span data-ttu-id="3fff6-169">Klikk på Tekstkonstant.</span><span class="sxs-lookup"><span data-stu-id="3fff6-169">Click Text constant.</span></span>
36. <span data-ttu-id="3fff6-170">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3fff6-170">In the list, mark the selected row.</span></span>
37. <span data-ttu-id="3fff6-171">Skriv inn en verdi i Tekst-feltet.</span><span class="sxs-lookup"><span data-stu-id="3fff6-171">In the Text field, type a value.</span></span>
38. <span data-ttu-id="3fff6-172">Klikk på Legg til.</span><span class="sxs-lookup"><span data-stu-id="3fff6-172">Click Add.</span></span>
39. <span data-ttu-id="3fff6-173">Klikk på Nummerserieverdi.</span><span class="sxs-lookup"><span data-stu-id="3fff6-173">Click Number sequence value.</span></span>
40. <span data-ttu-id="3fff6-174">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="3fff6-174">In the list, mark the selected row.</span></span>
41. <span data-ttu-id="3fff6-175">Angi eller velg en verdi i Nummerserieverdi-feltet.</span><span class="sxs-lookup"><span data-stu-id="3fff6-175">In the Number sequence field, enter or select a value.</span></span>
42. <span data-ttu-id="3fff6-176">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3fff6-176">Close the page.</span></span>
43. <span data-ttu-id="3fff6-177">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3fff6-177">Close the page.</span></span>
44. <span data-ttu-id="3fff6-178">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="3fff6-178">Close the page.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]