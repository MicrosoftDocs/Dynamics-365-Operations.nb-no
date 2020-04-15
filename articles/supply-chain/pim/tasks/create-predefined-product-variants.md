---
title: Opprette forhåndsdefinerte produktvarianter
description: Denne fremgangsmåten veileder deg gjennom oppretting av produktvarianter for en produktstandard ved hjelp av kombinasjoner av produktdimensjoner.
author: ShylaThompson
manager: AnnBe
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: EcoResProductListPage, EcoResProductCreate, EcoResProductDetails, EcoResProductMasterDimension, EcoResProductVariants, EcoResProductVariantSuggestions
audience: Application User
ms.reviewer: josaw
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: shylaw
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 678e2d7207628529530dcf3decd094583d3dff22
ms.sourcegitcommit: fcb27d6a46cd544feef34f6ec7607bdd46b0c12b
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 03/18/2020
ms.locfileid: "3150125"
---
# <a name="create-predefined-product-variants"></a><span data-ttu-id="11a07-103">Opprette forhåndsdefinerte produktvarianter</span><span class="sxs-lookup"><span data-stu-id="11a07-103">Create predefined product variants</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="11a07-104">Denne fremgangsmåten veileder deg gjennom oppretting av produktvarianter for en produktstandard ved hjelp av kombinasjoner av produktdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="11a07-104">This procedure walks through creating product variants for a product master using the combinations of product dimensions.</span></span> <span data-ttu-id="11a07-105">Demonstrasjonsfirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="11a07-105">The demo company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-master"></a><span data-ttu-id="11a07-106">Opprette en produktstandard</span><span class="sxs-lookup"><span data-stu-id="11a07-106">Create a product master</span></span>
1. <span data-ttu-id="11a07-107">Gå til Behandling av produktinformasjon > Produkter > Produktstandarder.</span><span class="sxs-lookup"><span data-stu-id="11a07-107">Go to Product information management > Products > Product masters.</span></span>
2. <span data-ttu-id="11a07-108">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="11a07-108">Click New.</span></span>
3. <span data-ttu-id="11a07-109">Skriv inn en verdi i feltet Produktnummer.</span><span class="sxs-lookup"><span data-stu-id="11a07-109">In the Product number field, type a value.</span></span>
    * <span data-ttu-id="11a07-110">Det er bare obligatorisk å angi et produktnummer manuelt hvis ingen nummerserie er definert for produktnummerfeltet.</span><span class="sxs-lookup"><span data-stu-id="11a07-110">Entering a product number manually is only required if no number sequence has been set for the product number field.</span></span> <span data-ttu-id="11a07-111">Hopp med andre ord over dette trinnet hvis nummerserien er definert for feltet.</span><span class="sxs-lookup"><span data-stu-id="11a07-111">In other words, skip the step if number sequence has been set for the field.</span></span>  
4. <span data-ttu-id="11a07-112">Skriv inn en verdi i feltet Produktnavn.</span><span class="sxs-lookup"><span data-stu-id="11a07-112">In the Product name field, type a value.</span></span>
5. <span data-ttu-id="11a07-113">Angi eller velg en verdi i Feltet Produktdimensjonsgruppe.</span><span class="sxs-lookup"><span data-stu-id="11a07-113">In the Product dimension group field, enter or select a value.</span></span>
    * <span data-ttu-id="11a07-114">Velg produktdimensjonsgruppen SizeCol (størrelse og farge).</span><span class="sxs-lookup"><span data-stu-id="11a07-114">Select the product dimension group SizeCol (Size and Color).</span></span>  
6. <span data-ttu-id="11a07-115">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="11a07-115">Click OK.</span></span>

## <a name="add-product-dimensions"></a><span data-ttu-id="11a07-116">Legge til produktdimensjoner</span><span class="sxs-lookup"><span data-stu-id="11a07-116">Add product dimensions</span></span>
1. <span data-ttu-id="11a07-117">Klikk Produktdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="11a07-117">Click Product dimensions.</span></span>
    * <span data-ttu-id="11a07-118">Dette eksemplet viser hvordan du manuelt angir produktdimensjoner.</span><span class="sxs-lookup"><span data-stu-id="11a07-118">This example shows how to manually enter product dimensions.</span></span> <span data-ttu-id="11a07-119">Du kan også velge en størrelse, farge eller stilgruppe som inkluderer produktdimensjonsverdiene du vil bruke.</span><span class="sxs-lookup"><span data-stu-id="11a07-119">You can also choose to select a size, color or style group that includes the product dimension values you want to use.</span></span>  
2. <span data-ttu-id="11a07-120">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="11a07-120">Click New.</span></span>
3. <span data-ttu-id="11a07-121">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="11a07-121">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="11a07-122">Angi eller velg en verdi i Størrelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="11a07-122">In the Size field, enter or select a value.</span></span>
5. <span data-ttu-id="11a07-123">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="11a07-123">In the Name field, type a value.</span></span>
6. <span data-ttu-id="11a07-124">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="11a07-124">Click New.</span></span>
7. <span data-ttu-id="11a07-125">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="11a07-125">In the list, mark the selected row.</span></span>
8. <span data-ttu-id="11a07-126">Angi eller velg en verdi i Størrelse-feltet.</span><span class="sxs-lookup"><span data-stu-id="11a07-126">In the Size field, enter or select a value.</span></span>
9. <span data-ttu-id="11a07-127">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="11a07-127">In the Name field, type a value.</span></span>
10. <span data-ttu-id="11a07-128">Klikk kategorien Farger.</span><span class="sxs-lookup"><span data-stu-id="11a07-128">Click the Colors tab.</span></span>
11. <span data-ttu-id="11a07-129">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="11a07-129">Click New.</span></span>
12. <span data-ttu-id="11a07-130">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="11a07-130">In the list, mark the selected row.</span></span>
13. <span data-ttu-id="11a07-131">Angi eller velg en verdi i feltet Farge.</span><span class="sxs-lookup"><span data-stu-id="11a07-131">In the Color field, enter or select a value.</span></span>
14. <span data-ttu-id="11a07-132">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="11a07-132">In the Name field, type a value.</span></span>
15. <span data-ttu-id="11a07-133">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="11a07-133">Click New.</span></span>
16. <span data-ttu-id="11a07-134">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="11a07-134">In the list, mark the selected row.</span></span>
17. <span data-ttu-id="11a07-135">Angi eller velg en verdi i feltet Farge.</span><span class="sxs-lookup"><span data-stu-id="11a07-135">In the Color field, enter or select a value.</span></span>
18. <span data-ttu-id="11a07-136">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="11a07-136">In the Name field, type a value.</span></span>
19. <span data-ttu-id="11a07-137">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="11a07-137">Click Save.</span></span>
20. <span data-ttu-id="11a07-138">Lukk siden.</span><span class="sxs-lookup"><span data-stu-id="11a07-138">Close the page.</span></span>

## <a name="generate-product-variants"></a><span data-ttu-id="11a07-139">Generere produktvarianter</span><span class="sxs-lookup"><span data-stu-id="11a07-139">Generate product variants</span></span>
1. <span data-ttu-id="11a07-140">Klikk Størrelser for produktvarianter.</span><span class="sxs-lookup"><span data-stu-id="11a07-140">Click Product variants.</span></span>
2. <span data-ttu-id="11a07-141">Klikk Variantforslag.</span><span class="sxs-lookup"><span data-stu-id="11a07-141">Click Variant suggestions.</span></span>
3. <span data-ttu-id="11a07-142">Klikk Velg alt.</span><span class="sxs-lookup"><span data-stu-id="11a07-142">Click Select all.</span></span>
    * <span data-ttu-id="11a07-143">I dette eksemplet velges alle mulige varianter.</span><span class="sxs-lookup"><span data-stu-id="11a07-143">In this example, all possible variants are selected.</span></span> <span data-ttu-id="11a07-144">Hvis bare et delsett av de mulige produktdimensjonskombinasjoner skal brukes for å opprette varianter, kan du velge de enkelte postene.</span><span class="sxs-lookup"><span data-stu-id="11a07-144">If only a subset of the possible product dimension combinations will be used to create variants, you can select the individual entries.</span></span>  
4. <span data-ttu-id="11a07-145">Klikk Opprett.</span><span class="sxs-lookup"><span data-stu-id="11a07-145">Click Create.</span></span>
    * <span data-ttu-id="11a07-146">Du kan generere beskrivelser for alle varianter basert på kombinasjonen av produktdimensjonsverdier.</span><span class="sxs-lookup"><span data-stu-id="11a07-146">You can generate descriptions for all your variants based on the combination of product dimension values.</span></span> <span data-ttu-id="11a07-147">Beskrivelser er valgfritt.</span><span class="sxs-lookup"><span data-stu-id="11a07-147">The descriptions are optional.</span></span>  
5. <span data-ttu-id="11a07-148">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="11a07-148">Click Save.</span></span>

