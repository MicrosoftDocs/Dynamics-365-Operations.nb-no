---
title: Opprette en produktkonfigurasjonsmodell
description: Denne prosedyren viser hvordan du oppretter en produktkonfigurasjonsmodell og angir grunnleggende opplysninger, for eksempel attributter og delkomponenter.
author: ShylaThompson
ms.date: 08/29/2018
ms.topic: business-process
ms.prod: ''
ms.technology: ''
ms.search.form: DefaultDashboard, EcoResProductVariantMaintainWorkspace, PCProductConfigurationModelListPage, PCCreateProductConfigurationModel, PCProductConfigurationModelDetails, PCBOMLineDetails
audience: Application User
ms.reviewer: kamaybac
ms.search.region: Global
ms.author: kamaybac
ms.search.validFrom: 2016-06-30
ms.dyn365.ops.version: Version 7.0.0
ms.openlocfilehash: 2cb9e33d7bab6ca9cd378ec40baa796d1a933ece
ms.sourcegitcommit: fa99a36c3d30d0c0577fd3f63ed6bf2f71599e40
ms.translationtype: HT
ms.contentlocale: nb-NO
ms.lasthandoff: 04/20/2021
ms.locfileid: "5921371"
---
# <a name="create-a-product-configuration-model"></a><span data-ttu-id="f267c-103">Opprette en produktkonfigurasjonsmodell</span><span class="sxs-lookup"><span data-stu-id="f267c-103">Create a product configuration model</span></span>

[!include [banner](../../includes/banner.md)]

<span data-ttu-id="f267c-104">Denne prosedyren viser hvordan du oppretter en produktkonfigurasjonsmodell og angir grunnleggende opplysninger, for eksempel attributter og delkomponenter.</span><span class="sxs-lookup"><span data-stu-id="f267c-104">This procedure shows how to create a product configuration model and enter basic information such as attributes and subcomponents.</span></span> <span data-ttu-id="f267c-105">Demonstrasjonsdatafirmaet USMF brukes til å opprette denne fremgangsmåten.</span><span class="sxs-lookup"><span data-stu-id="f267c-105">The demo data company used to create this procedure is USMF.</span></span>


## <a name="create-a-product-model"></a><span data-ttu-id="f267c-106">Opprette en produktmodell</span><span class="sxs-lookup"><span data-stu-id="f267c-106">Create a product model</span></span>

1. <span data-ttu-id="f267c-107">Gå til **Behandling av produktinformasjon \> Produkter \> Produktkonfigurasjonsmodeller**.</span><span class="sxs-lookup"><span data-stu-id="f267c-107">Go to **Product information management \> Products \> Product configuration models**.</span></span>
1. <span data-ttu-id="f267c-108">Velg **Ny**.</span><span class="sxs-lookup"><span data-stu-id="f267c-108">Select **New**.</span></span>
1. <span data-ttu-id="f267c-109">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f267c-109">In the **Name** field, type a value.</span></span>
1. <span data-ttu-id="f267c-110">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f267c-110">In the **Description** field, type a value.</span></span>
1. <span data-ttu-id="f267c-111">Velg et alternativ i feltet **Problemløserstrategi**.</span><span class="sxs-lookup"><span data-stu-id="f267c-111">In the **Solver strategy** field, select an option.</span></span>
    * <span data-ttu-id="f267c-112">Problemløserstrategien bestemmer hvordan restriksjonene i en restriksjonsbasert produktkonfigurasjonsmodell skal behandles.</span><span class="sxs-lookup"><span data-stu-id="f267c-112">The solver strategy determines how the constraints in a constraint-based product configuration model are processed.</span></span> <span data-ttu-id="f267c-113">Dette valget kan ha innvirkning på ytelsen til produktkonfigurasjonsmodellen.</span><span class="sxs-lookup"><span data-stu-id="f267c-113">This selection can have an impact on the performance of the product configuration model.</span></span>  
1. <span data-ttu-id="f267c-114">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f267c-114">In the **Name** field, type a value.</span></span>
    * <span data-ttu-id="f267c-115">Rotkomponenten representerer produktkonfigurasjonsmodellen, men den kan også brukes i andre produktmodeller.</span><span class="sxs-lookup"><span data-stu-id="f267c-115">The root component represents the product configuration model, but it can also be used in other product models.</span></span>  
1. <span data-ttu-id="f267c-116">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f267c-116">Select **OK**.</span></span>
1. <span data-ttu-id="f267c-117">Velg et alternativ i feltet **Bruk konfigurasjoner** på nytt.</span><span class="sxs-lookup"><span data-stu-id="f267c-117">In the **Reuse configurations** field, select an option.</span></span>
    * <span data-ttu-id="f267c-118">Hvis parameteren Bruk konfigurasjoner på nytt er satt til Ja, kontrollerer systemet for identiske konfigurasjoner etter hver konfigurasjonsøkt og bruker dem på nytt hvis det blir funnet et nøyaktig samsvar.</span><span class="sxs-lookup"><span data-stu-id="f267c-118">If the reuse configurations parameter is set to Yes, the system will check for identical configurations after each configuration session and reuse if an exact match is found.</span></span>  

## <a name="add-attributes"></a><span data-ttu-id="f267c-119">Legg til attributter</span><span class="sxs-lookup"><span data-stu-id="f267c-119">Add attributes</span></span>

1. <span data-ttu-id="f267c-120">Utvid delen **Attributter**.</span><span class="sxs-lookup"><span data-stu-id="f267c-120">Expand the **Attributes** section.</span></span>
2. <span data-ttu-id="f267c-121">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="f267c-121">Select **Add**.</span></span>
3. <span data-ttu-id="f267c-122">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f267c-122">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f267c-123">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f267c-123">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="f267c-124">Skriv inn en verdi i feltet **Problemløsernavn**.</span><span class="sxs-lookup"><span data-stu-id="f267c-124">In the **Solver name** field, type a value.</span></span>
    * <span data-ttu-id="f267c-125">Problemløsernavnet brukes i problemløseren for begrensning for produktkonfiguratoren.</span><span class="sxs-lookup"><span data-stu-id="f267c-125">The solver name is used by the constraint solver of the product configurator.</span></span> <span data-ttu-id="f267c-126">Det må ikke inneholde mellomrom eller spesialtegn med unntak av _ (understrekingstegn).</span><span class="sxs-lookup"><span data-stu-id="f267c-126">It must not include spaces or special characters except _ (underscore).</span></span>  
6. <span data-ttu-id="f267c-127">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f267c-127">In the **Description** field, type a value.</span></span>
    * <span data-ttu-id="f267c-128">Den beskrivende teksten vises for konfigurasjonsbrukeren, og kan derfor fungere som hjelp til å velge riktig attributtverdi.</span><span class="sxs-lookup"><span data-stu-id="f267c-128">The description text is displayed to the configuration user and can therefore serve as help in selecting the right attribute value.</span></span>  
7. <span data-ttu-id="f267c-129">Angi eller velg en verdi i **Attributtype**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f267c-129">In the **Attribute type** field, enter or select a value.</span></span>
    * <span data-ttu-id="f267c-130">Attributtypen bestemmer hvilke verdier som er tilgjengelige for attributtet.</span><span class="sxs-lookup"><span data-stu-id="f267c-130">The attribute type determines which values are available for the attribute.</span></span>  
8. <span data-ttu-id="f267c-131">Merk av for **Ta med i gjenbruk**.</span><span class="sxs-lookup"><span data-stu-id="f267c-131">Select the **Include in reuse** check box.</span></span>
    * <span data-ttu-id="f267c-132">Dette alternativet er bare tilgjengelig når alternativet Bruk konfigurasjoner på nytt er valgt.</span><span class="sxs-lookup"><span data-stu-id="f267c-132">This option is only available when the Reuse configurations option is selected.</span></span> <span data-ttu-id="f267c-133">Når du inkluderer attributtet i avmerkingsboksen for gjenbruk, betyr det at attributtet vurderes når systemet søker etter et nøyaktig samsvar.</span><span class="sxs-lookup"><span data-stu-id="f267c-133">Including the attribute in the reuse check box means that this attribute will be considered when the system is looking for an exact match.</span></span>  

## <a name="add-subcomponents"></a><span data-ttu-id="f267c-134">Legge til delkomponenter</span><span class="sxs-lookup"><span data-stu-id="f267c-134">Add subcomponents</span></span>

1. <span data-ttu-id="f267c-135">Utvid delen **Underkomponenter**.</span><span class="sxs-lookup"><span data-stu-id="f267c-135">Expand the **Subcomponents** section.</span></span>
2. <span data-ttu-id="f267c-136">Velg **Legg til**.</span><span class="sxs-lookup"><span data-stu-id="f267c-136">Select **Add**.</span></span>
3. <span data-ttu-id="f267c-137">Merk den valgte raden i listen.</span><span class="sxs-lookup"><span data-stu-id="f267c-137">In the list, mark the selected row.</span></span>
4. <span data-ttu-id="f267c-138">Skriv inn en verdi i **Navn**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f267c-138">In the **Name** field, type a value.</span></span>
5. <span data-ttu-id="f267c-139">Skriv inn en verdi i feltet **Problemløsernavn**.</span><span class="sxs-lookup"><span data-stu-id="f267c-139">In the **Solver name** field, type a value.</span></span>
6. <span data-ttu-id="f267c-140">Skriv inn en verdi i **Beskrivelse**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f267c-140">In the **Description** field, type a value.</span></span>
7. <span data-ttu-id="f267c-141">Angi eller velg en verdi i feltet **Komponent**.</span><span class="sxs-lookup"><span data-stu-id="f267c-141">In the **Component** field, enter or select a value.</span></span>
    * <span data-ttu-id="f267c-142">Hver underkomponent må referere til en komponentdefinisjon.</span><span class="sxs-lookup"><span data-stu-id="f267c-142">Each subcomponent must reference a component definition.</span></span> <span data-ttu-id="f267c-143">Denne utformingen støtter gjenbrukbare komponenter og sikrer at når en komponent er definert, så kan den brukes i mange produktmodeller.</span><span class="sxs-lookup"><span data-stu-id="f267c-143">This design supports reusable components and ensures that once a component has been defined it can be used in many product models.</span></span>  
8. <span data-ttu-id="f267c-144">Velg **Lagre**.</span><span class="sxs-lookup"><span data-stu-id="f267c-144">Select **Save**.</span></span>
9. <span data-ttu-id="f267c-145">Velg **Stykklistelinjedetaljer**.</span><span class="sxs-lookup"><span data-stu-id="f267c-145">Select **BOM line details**.</span></span>
    * <span data-ttu-id="f267c-146">I skjemaet Detaljer om stykklistelinje kan brukeren velge de nødvendige egenskapene for delkomponenten.</span><span class="sxs-lookup"><span data-stu-id="f267c-146">The BOM line details form enables the user to select the required properties for the subcomponent.</span></span> <span data-ttu-id="f267c-147">Hver egenskap kan gis en fast verdi eller tilordnes til et attributt.</span><span class="sxs-lookup"><span data-stu-id="f267c-147">Each property can be given a fixed value or mapped to an attribute.</span></span> <span data-ttu-id="f267c-148">Tilordning til et attributt fører til at egenskapen Stykklistelinje får ulike verdier avhengig av konfigurasjonsvalget.</span><span class="sxs-lookup"><span data-stu-id="f267c-148">Mapping to an attribute will result in the BOM line property getting different values depending on the configuration selection.</span></span>  
10. <span data-ttu-id="f267c-149">Angi eller velg en verdi i **Varenummer**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f267c-149">In the **Item number** field, enter or select a value.</span></span>
    * <span data-ttu-id="f267c-150">Hver underkomponent representerer en konfigurerbar produktstandard med teknologi for restriksjonsbasert konfigurasjon.</span><span class="sxs-lookup"><span data-stu-id="f267c-150">Each subcomponent represents a configurable product master with constraint-based configuration technology.</span></span> <span data-ttu-id="f267c-151">Referansen utføres via varenummeret.</span><span class="sxs-lookup"><span data-stu-id="f267c-151">The reference is made through the item number.</span></span>  
11. <span data-ttu-id="f267c-152">Merk av for **Sett**.</span><span class="sxs-lookup"><span data-stu-id="f267c-152">Select the **Set** check box.</span></span>
12. <span data-ttu-id="f267c-153">Velg **Ja** i feltet **Beregning**.</span><span class="sxs-lookup"><span data-stu-id="f267c-153">Select **Yes** in the **Calculation** field.</span></span>
    * <span data-ttu-id="f267c-154">Når du angir beregningsalternativet, sikrer du at produktet vil bli inkludert når du kjører en kostberegning for produktet.</span><span class="sxs-lookup"><span data-stu-id="f267c-154">Setting the calculation option ensures that the product will be included when running a cost calculation for the product.</span></span>  
13. <span data-ttu-id="f267c-155">Velg **Oppsett**-fanen.</span><span class="sxs-lookup"><span data-stu-id="f267c-155">Select the **Setup** tab.</span></span>
14. <span data-ttu-id="f267c-156">Merk av for **Sett**.</span><span class="sxs-lookup"><span data-stu-id="f267c-156">Select the **Set** check box.</span></span>
15. <span data-ttu-id="f267c-157">Angi et tall i **Antall**-feltet.</span><span class="sxs-lookup"><span data-stu-id="f267c-157">In the **Quantity** field, enter a number.</span></span>
    * <span data-ttu-id="f267c-158">Antall-feltet bestemmer hvor mye av dette produktet som skal forbrukes i det konfigurerte produktet.</span><span class="sxs-lookup"><span data-stu-id="f267c-158">The quantity field determines how much of this product will be consumed in the configured product.</span></span>  
16. <span data-ttu-id="f267c-159">Merk av for **Sett**.</span><span class="sxs-lookup"><span data-stu-id="f267c-159">Select the **Set** check box.</span></span>
17. <span data-ttu-id="f267c-160">Angi et tall i feltet **Per serie**.</span><span class="sxs-lookup"><span data-stu-id="f267c-160">In the **Per series** field, enter a number.</span></span>
18. <span data-ttu-id="f267c-161">Velg **OK**.</span><span class="sxs-lookup"><span data-stu-id="f267c-161">Select **OK**.</span></span>



[!INCLUDE[footer-include](../../../includes/footer-banner.md)]