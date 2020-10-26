---
title: Opprette en produktkonfigurasjonsmodell
description: Denne prosedyren viser hvordan du oppretter en produktkonfigurasjonsmodell og angir grunnleggende opplysninger, for eksempel attributter og delkomponenter.
author: ShylaThompson
manager: tfehr
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.service: dynamics-ax-applications
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.scope: Core, Operations
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 9c81b3af7460c636245dcc16affcb05b724fbc70
ms.sourcegitcommit: 708ca25687a4e48271cdcd6d2d22d99fb94cf140
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 10/10/2020
ms.locfileid: "3986125"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="a15f0-103">Opprette en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="a15f0-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="a15f0-104">Denne prosedyren viser hvordan du oppretter en produktkonfigurasjonsmodell og angir grunnleggende opplysninger, for eksempel attributter og delkomponenter.</span><span class="sxs-lookup"><span data-stu-id="a15f0-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="a15f0-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="a15f0-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="a15f0-106">Opprette en produktmodell</span><span class="sxs-lookup"><span data-stu-id="a15f0-106">Create a product model</span></span>
1. <span data-ttu-id="a15f0-107">Klikk Definisjon av produktvariantmodell.</span><span class="sxs-lookup"><span data-stu-id="a15f0-107">Click Product variant model definition.</span></span>
2. <span data-ttu-id="a15f0-108">Klikk Produktkonfigurasjonsmodeller.</span><span class="sxs-lookup"><span data-stu-id="a15f0-108">Click Product configuration models.</span></span>
3. <span data-ttu-id="a15f0-109">Klikk Ny.</span><span class="sxs-lookup"><span data-stu-id="a15f0-109">Click New.</span></span>
4. <span data-ttu-id="a15f0-110">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a15f0-110">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a15f0-111">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="a15f0-111">In the Description field, type a value.</span></span>
6. <span data-ttu-id="a15f0-112">Velg et alternativ i feltet Problemløserstrategi.</span><span class="sxs-lookup"><span data-stu-id="a15f0-112">In the Solver strategy field, select an option.</span></span>
    * <span data-ttu-id="a15f0-113">Problemløserstrategien bestemmer hvordan restriksjonene i en restriksjonsbasert produktkonfigurasjonsmodell skal behandles.</span><span class="sxs-lookup"><span data-stu-id="a15f0-113">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="a15f0-114">Dette valget kan ha innvirkning på ytelsen til produktkonfigurasjonsmodellen.</span><span class="sxs-lookup"><span data-stu-id="a15f0-114">This selection can have an impact on the performance of the product configuration model.</span></span>  
7. <span data-ttu-id="a15f0-115">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a15f0-115">In the Name field, type a value.</span></span>
    * <span data-ttu-id="a15f0-116">Rotkomponenten representerer produktkonfigurasjonsmodellen, men den kan også brukes i andre produktmodeller.</span><span class="sxs-lookup"><span data-stu-id="a15f0-116">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
8. <span data-ttu-id="a15f0-117">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a15f0-117">Click OK.</span></span>
9. <span data-ttu-id="a15f0-118">Velg et alternativ i feltet Bruk konfigurasjoner på nytt.</span><span class="sxs-lookup"><span data-stu-id="a15f0-118">In the Reuse configurations field, select an option.</span></span>
    * <span data-ttu-id="a15f0-119">Hvis parameteren Bruk konfigurasjoner på nytt er satt til Ja, kontrollerer systemet for identiske konfigurasjoner etter hver konfigurasjonsøkt og bruker dem på nytt hvis det blir funnet et nøyaktig samsvar.</span><span class="sxs-lookup"><span data-stu-id="a15f0-119">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="a15f0-120">Legg til attributter</span><span class="sxs-lookup"><span data-stu-id="a15f0-120">Add attributes</span></span>
1. <span data-ttu-id="a15f0-121">Utvid delen Attributter.</span><span class="sxs-lookup"><span data-stu-id="a15f0-121">Expand the Attributes section.</span></span>
2. <span data-ttu-id="a15f0-122">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="a15f0-122">Click Add.</span></span>
3. <span data-ttu-id="a15f0-123">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a15f0-123">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a15f0-124">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a15f0-124">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a15f0-125">Skriv inn en verdi i feltet Problemløsernavn.</span><span class="sxs-lookup"><span data-stu-id="a15f0-125">In the Solver name field, type a value.</span></span>
    * <span data-ttu-id="a15f0-126">Problemløsernavnet brukes i problemløseren for begrensning for produktkonfiguratoren.</span><span class="sxs-lookup"><span data-stu-id="a15f0-126">The Solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="a15f0-127">Det må ikke inneholde mellomrom eller spesialtegn med unntak av _ (understrekingstegn).</span><span class="sxs-lookup"><span data-stu-id="a15f0-127">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="a15f0-128">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="a15f0-128">In the Description field, type a value.</span></span>
    * <span data-ttu-id="a15f0-129">Den beskrivende teksten vises for konfigurasjonsbrukeren, og kan derfor fungere som hjelp til å velge riktig attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="a15f0-129">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="a15f0-130">Angi eller velg en verdi i Attributtype-feltet.</span><span class="sxs-lookup"><span data-stu-id="a15f0-130">In the Attribute type field, enter or select a value.</span></span>
    * <span data-ttu-id="a15f0-131">Attributtypen bestemmer hvilke verdier som er tilgjengelige for attributtet.</span><span class="sxs-lookup"><span data-stu-id="a15f0-131">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="a15f0-132">Merk av for Ta med i gjenbruk.</span><span class="sxs-lookup"><span data-stu-id="a15f0-132">Select the Include in reuse check box.</span></span>
    * <span data-ttu-id="a15f0-133">Dette alternativet er bare tilgjengelig når alternativet Bruk konfigurasjoner på nytt er valgt.</span><span class="sxs-lookup"><span data-stu-id="a15f0-133">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="a15f0-134">Når du inkluderer attributtet i avmerkingsboksen for gjenbruk, betyr det at attributtet vurderes når systemet søker etter et nøyaktig samsvar.</span><span class="sxs-lookup"><span data-stu-id="a15f0-134">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="a15f0-135">Legge til delkomponenter</span><span class="sxs-lookup"><span data-stu-id="a15f0-135">Add subcomponents</span></span>
1. <span data-ttu-id="a15f0-136">Utvid delen Underkomponenter.</span><span class="sxs-lookup"><span data-stu-id="a15f0-136">Expand the Subcomponents section.</span></span>
2. <span data-ttu-id="a15f0-137">Klikk Legg til.</span><span class="sxs-lookup"><span data-stu-id="a15f0-137">Click Add.</span></span>
3. <span data-ttu-id="a15f0-138">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="a15f0-138">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="a15f0-139">Skriv inn en verdi i Navn-feltet.</span><span class="sxs-lookup"><span data-stu-id="a15f0-139">In the Name field, type a value.</span></span>
5. <span data-ttu-id="a15f0-140">Skriv inn en verdi i feltet Problemløsernavn.</span><span class="sxs-lookup"><span data-stu-id="a15f0-140">In the Solver name field, type a value.</span></span>
6. <span data-ttu-id="a15f0-141">Skriv inn en verdi i feltet Beskrivelse.</span><span class="sxs-lookup"><span data-stu-id="a15f0-141">In the Description field, type a value.</span></span>
7. <span data-ttu-id="a15f0-142">Angi eller velg en verdi i feltet Komponent.</span><span class="sxs-lookup"><span data-stu-id="a15f0-142">In the Component field, enter or select a value.</span></span>
    * <span data-ttu-id="a15f0-143">Hver underkomponent må referere til en komponentdefinisjon.</span><span class="sxs-lookup"><span data-stu-id="a15f0-143">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="a15f0-144">Denne utformingen støtter gjenbrukbare komponenter og sikrer at når en komponent er definert, så kan den brukes i mange produktmodeller.</span><span class="sxs-lookup"><span data-stu-id="a15f0-144">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="a15f0-145">Klikk Lagre.</span><span class="sxs-lookup"><span data-stu-id="a15f0-145">Click Save.</span></span>
9. <span data-ttu-id="a15f0-146">Klikk Detaljer om stykklistelinje.</span><span class="sxs-lookup"><span data-stu-id="a15f0-146">Click BOM line details.</span></span>
    * <span data-ttu-id="a15f0-147">I skjemaet Detaljer om stykklistelinje kan brukeren velge de nødvendige egenskapene for delkomponenten.</span><span class="sxs-lookup"><span data-stu-id="a15f0-147">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="a15f0-148">Hver egenskap kan gis en fast verdi eller tilordnes til et attributt.</span><span class="sxs-lookup"><span data-stu-id="a15f0-148">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="a15f0-149">Tilordning til et attributt fører til at egenskapen Stykklistelinje får ulike verdier avhengig av konfigurasjonsvalget.</span><span class="sxs-lookup"><span data-stu-id="a15f0-149">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="a15f0-150">Angi eller velg en verdi i Varenummer-feltet.</span><span class="sxs-lookup"><span data-stu-id="a15f0-150">In the Item number field, enter or select a value.</span></span>
    * <span data-ttu-id="a15f0-151">Hver underkomponent representerer en konfigurerbar produktstandard med teknologi for restriksjonsbasert konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="a15f0-151">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="a15f0-152">Referansen utføres via varenummeret.</span><span class="sxs-lookup"><span data-stu-id="a15f0-152">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="a15f0-153">Merk av for Sett.</span><span class="sxs-lookup"><span data-stu-id="a15f0-153">Select the Set check box.</span></span>
12. <span data-ttu-id="a15f0-154">Velg Ja i feltet Beregning.</span><span class="sxs-lookup"><span data-stu-id="a15f0-154">Select Yes in the Calculation field.</span></span>
    * <span data-ttu-id="a15f0-155">Når du angir beregningsalternativet, sikrer du at produktet vil bli inkludert når du kjører en kostberegning for produktet.</span><span class="sxs-lookup"><span data-stu-id="a15f0-155">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="a15f0-156">Klikk kategorien Oppsett.</span><span class="sxs-lookup"><span data-stu-id="a15f0-156">Click the Setup tab.</span></span>
14. <span data-ttu-id="a15f0-157">Merk av for Sett.</span><span class="sxs-lookup"><span data-stu-id="a15f0-157">Select the Set check box.</span></span>
15. <span data-ttu-id="a15f0-158">Angi et tall i feltet Antall.</span><span class="sxs-lookup"><span data-stu-id="a15f0-158">In the Quantity field, enter a number.</span></span>
    * <span data-ttu-id="a15f0-159">Antall-feltet bestemmer hvor mye av dette produktet som skal forbrukes i det konfigurerte produktet.</span><span class="sxs-lookup"><span data-stu-id="a15f0-159">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="a15f0-160">Merk av for Sett.</span><span class="sxs-lookup"><span data-stu-id="a15f0-160">Select the Set check box.</span></span>
17. <span data-ttu-id="a15f0-161">Angi et tall i feltet Per serie.</span><span class="sxs-lookup"><span data-stu-id="a15f0-161">In the Per series field, enter a number.</span></span>
18. <span data-ttu-id="a15f0-162">Klikk OK.</span><span class="sxs-lookup"><span data-stu-id="a15f0-162">Click OK.</span></span>

